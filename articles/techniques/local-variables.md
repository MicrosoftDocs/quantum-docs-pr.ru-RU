---
title: 'Методы Q # — локальные переменные | Документация Майкрософт'
description: 'Методы Q # — локальные переменные'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4f5eff1ee8482fa5e5fee9dff421efab93fc0c5a
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183290"
---
# <a name="local-variables"></a><span data-ttu-id="099ab-103">Локальные переменные</span><span class="sxs-lookup"><span data-stu-id="099ab-103">Local Variables</span></span> #

<span data-ttu-id="099ab-104">Значение любого типа в Q # можно присвоить переменной для повторного использования в операции или функции с помощью ключевого слова `let`.</span><span class="sxs-lookup"><span data-stu-id="099ab-104">A value of any type in Q# can be assigned to a variable for reuse within an operation or function by using the `let` keyword.</span></span>
<span data-ttu-id="099ab-105">Например:</span><span class="sxs-lookup"><span data-stu-id="099ab-105">For instance:</span></span>

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

<span data-ttu-id="099ab-106">Это назначает определенный массив операторов Паули переменной с именем `measurementOperator`.</span><span class="sxs-lookup"><span data-stu-id="099ab-106">This assigns a particular array of Pauli operators to a variable called `measurementOperator`.</span></span>

> [!TIP]
> <span data-ttu-id="099ab-107">Обратите внимание, что нам не нужно явно указывать тип нашей новой переменной, так как выражение в правой части оператора `let` является неоднозначным и тип выводится компилятором.</span><span class="sxs-lookup"><span data-stu-id="099ab-107">Note that we did not need to explicitly specify the type of our new variable, as the expression on the right-hand side of the `let` statement is unambiguous and the type is inferred by the compiler.</span></span> 

<span data-ttu-id="099ab-108">Переменные в Q # являются *неизменяемыми*. Это означает, что после того как переменная определена таким образом, она больше не может быть изменена каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="099ab-108">Variables in Q# are *immutable*, meaning that once a variable has been defined in this way, it can no longer be changed in any way.</span></span>
<span data-ttu-id="099ab-109">Это обеспечивает несколько выгодных оптимизаций, включая оптимизацию классической логики, действующей на переменные, для изменения порядка применения `Adjoint` варианта операции.</span><span class="sxs-lookup"><span data-stu-id="099ab-109">This allows for several beneficial optimizations, including optimization of the classical logic acting on variables to be reordered for applying the `Adjoint` variant of an operation.</span></span>

<span data-ttu-id="099ab-110">Переменные, определенные с помощью привязки `let`, как и выше, являются локальными для определенной области, например тело операции или содержимое цикла `for`.</span><span class="sxs-lookup"><span data-stu-id="099ab-110">Variables defined using the `let` binding as above are local to a particular scope, such as the body of an operation or the contents of a `for` loop.</span></span>


## <a name="mutability"></a><span data-ttu-id="099ab-111">Измен</span><span class="sxs-lookup"><span data-stu-id="099ab-111">Mutability</span></span> ##

<span data-ttu-id="099ab-112">В качестве альтернативы созданию переменной с `let`ключевое слово `mutable` создаст специальную изменяемую переменную, которая может быть повторно привязана после первоначального создания с помощью ключевого слова `set`.</span><span class="sxs-lookup"><span data-stu-id="099ab-112">As an alternative to creating a variable with `let`, the `mutable` keyword will create a special mutable variable that can be re-bound after it is initially created by using the `set` keyword.</span></span>

```qsharp
operation RandomInts(maxInt : Int, nrSamples : Int) : Int[] {
    mutable samples = new Int[0];
    for (i in 1 .. nrSamples) {
        set samples += [RandomInt(maxInt)];
    }
    return samples;
}
```

<span data-ttu-id="099ab-113">Все типы в Q #, включая массивы, следуют семантике значений.</span><span class="sxs-lookup"><span data-stu-id="099ab-113">All types in Q#, including arrays, follow value semantics.</span></span> <span data-ttu-id="099ab-114">В частности, невозможно обновить элементы массива.</span><span class="sxs-lookup"><span data-stu-id="099ab-114">In particular, it is not possible to update array items.</span></span> <span data-ttu-id="099ab-115">Чтобы изменить существующий массив, необходимо использовать механизм копирования и обновления, похожий на один для записей в F#.</span><span class="sxs-lookup"><span data-stu-id="099ab-115">To modify an existing array requires leveraging a copy-and-update mechanism much like the one for records in F#.</span></span> <span data-ttu-id="099ab-116">Используя средства библиотеки для массивов, предоставляемых в [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), мы можем, например, легко определить функцию, возвращающую массив пола, где Паули по индексу `i` принимает заданное значение, а все остальные записи являются идентификатором:</span><span class="sxs-lookup"><span data-stu-id="099ab-116">Using the library tools for arrays provided in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), we can e.g. easily define a function that returns an array of Paulis where the Pauli at index `i` takes the given value and all other entries are the identity:</span></span> 

```qsharp
function EmbedPauli (pauli : Pauli, i : Int, n : Int) : Pauli[] {
    
    let arr = ConstantArray(n, PauliI); // creates an array of filled with PauliI
    return arr w/ i <- pauli; // constructs a new array based on arr except that entry i is set to pauli
}
```

<span data-ttu-id="099ab-117">Мы подробнее рассмотрим работу с массивами при обсуждении инструкций и выражений Q #.</span><span class="sxs-lookup"><span data-stu-id="099ab-117">We will elaborate more on how to work with arrays when discussing Q# statements and expressions.</span></span> 

<span data-ttu-id="099ab-118">Изменяемость в Q # — это концепция, которая применяется к *символу* , а не к типу или значению.</span><span class="sxs-lookup"><span data-stu-id="099ab-118">Mutability within Q# is a concept that applies to a *symbol* rather than a type or value.</span></span> <span data-ttu-id="099ab-119">В частности, он не имеет представления в системе типов, неявно или явно, а также от того, является ли привязка изменяемой (как указано ключевым словом `mutable`) или неизменяемой (как указано в `let`), не изменяет тип привязанных переменных.</span><span class="sxs-lookup"><span data-stu-id="099ab-119">Specifically, it does not have a representation in the type system, implicitly or explicitly, and whether or not a binding is mutable (as indicated by the `mutable` keyword) or immutable (as indicated by `let`) does not change the type of the bound variable(s).</span></span> <span data-ttu-id="099ab-120">Это обеспечивает важный способ изоляции изменяемых функций в специализированных функциях и операциях.</span><span class="sxs-lookup"><span data-stu-id="099ab-120">This provides an important way to isolate mutability inside specialized functions and operations.</span></span>
<span data-ttu-id="099ab-121">В частности, несмотря на то, что во внешней специализации для операции, которая использует изменяемую переменную, не может быть создана автоматически, автоматическое создание автоматически выполняется для операции, вызывающей функцию, которая использует mutable.</span><span class="sxs-lookup"><span data-stu-id="099ab-121">In particular, even though an adjoint specialization for an operation which uses a mutable variable cannot be auto-generated, auto-generation works fine for an operation calling a function which uses mutability.</span></span>
<span data-ttu-id="099ab-122">По этой причине рекомендуется сделать функции и операции, которые используют изменяемость, как можно меньшее и сжимать, чтобы остальная часть тактовой программы могла быть написана с использованием обычных неизменяемых переменных.</span><span class="sxs-lookup"><span data-stu-id="099ab-122">For this reason, it is a good practice to make functions and operations which use mutability as short and compact as possible, so that the rest of the quantum program can be written using ordinary immutable variables.</span></span>


## <a name="deconstruction"></a><span data-ttu-id="099ab-123">Деконструкция</span><span class="sxs-lookup"><span data-stu-id="099ab-123">Deconstruction</span></span> ##

<span data-ttu-id="099ab-124">Помимо присвоения одной переменной, `let` и `mutable` ключевые слова — или на самом деле любые другие конструкции привязки — также позволяют распаковать содержимое [типа кортежа](xref:microsoft.quantum.language.type-model#tuple-types).</span><span class="sxs-lookup"><span data-stu-id="099ab-124">In addition to assigning a single variable, the `let` and `mutable` keywords - or in fact any other binding construct - also allow for unpacking the contents of a [tuple type](xref:microsoft.quantum.language.type-model#tuple-types).</span></span>
<span data-ttu-id="099ab-125">Назначение этой формы называется *деконструированием* элементов этого кортежа.</span><span class="sxs-lookup"><span data-stu-id="099ab-125">An assignment of this form is said to *deconstruct* the elements of that tuple.</span></span>
<span data-ttu-id="099ab-126">Например, если мы моделируем термин в Хамилтониан с помощью кортежа, то мы можем использовать деконструкцию для доступа к различным данным, которые необходимо смоделировать под этим термином:</span><span class="sxs-lookup"><span data-stu-id="099ab-126">For instance, if we model a term in a Hamiltonian by a tuple, then we can use deconstruction to access the different data that we need to simulate under that term:</span></span>

```qsharp
// Represents H = 3.1 X_0 Z_1.
let (_, (paulis, idxQubits)) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // paulis and idxQubits are both immutable variables
mutable ((c1, c2), _) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // c1 and c2 are both mutable variables
```


