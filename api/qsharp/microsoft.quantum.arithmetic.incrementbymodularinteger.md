---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Операция Инкрементбимодуларинтежер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 8a02d22facce8f58180752b6d063ac55d75ca537
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222955"
---
# <a name="incrementbymodularinteger-operation"></a><span data-ttu-id="390a1-102">Операция Инкрементбимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="390a1-102">IncrementByModularInteger operation</span></span>

<span data-ttu-id="390a1-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="390a1-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="390a1-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="390a1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="390a1-105">Выполняет модульное увеличение регистра кубит с помощью целочисленной константы.</span><span class="sxs-lookup"><span data-stu-id="390a1-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="390a1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="390a1-106">Description</span></span>

<span data-ttu-id="390a1-107">Отметим, `increment` что $a $, `modulus` $N $ и целое число, закодированные `target` $y $.</span><span class="sxs-lookup"><span data-stu-id="390a1-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="390a1-108">Затем операция выполняет следующее преобразование: \бегин{алигн} \кет{и} \мапсто \кет{(y + a) \операторнаме{мод} N} \енд{алигн} целые числа кодируются в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="390a1-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format.</span></span>

## <a name="input"></a><span data-ttu-id="390a1-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="390a1-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="390a1-110">приращение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="390a1-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="390a1-111">Целочисленное приращение $a $, добавляемое в $y $.</span><span class="sxs-lookup"><span data-stu-id="390a1-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="390a1-112">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="390a1-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="390a1-113">Integer $N $, МОДС $y + a $.</span><span class="sxs-lookup"><span data-stu-id="390a1-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="390a1-114">Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="390a1-114">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="390a1-115">Целочисленный $y $ в `LittleEndian` формате, `increment` к которому добавляется $a $.</span><span class="sxs-lookup"><span data-stu-id="390a1-115">Integer $y$ in `LittleEndian` format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="390a1-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="390a1-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="390a1-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="390a1-117">Remarks</span></span>

<span data-ttu-id="390a1-118">Предполагается, что начальное значение целевого объекта меньше $N $, а шаг приращения $a $ меньше $N $.</span><span class="sxs-lookup"><span data-stu-id="390a1-118">Assumes that the initial value of target is less than $N$ and that the increment $a$ is less than $N$.</span></span>
<span data-ttu-id="390a1-119">Обратите внимание, что <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> реализует ту же операцию на `PhaseLittleEndian` основе.</span><span class="sxs-lookup"><span data-stu-id="390a1-119">Note that <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> implements the same operation in the `PhaseLittleEndian` basis.</span></span>

## <a name="see-also"></a><span data-ttu-id="390a1-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="390a1-120">See Also</span></span>

- [<span data-ttu-id="390a1-121">Microsoft. тактов. арифметик. Инкрементфасебимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="390a1-121">Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)