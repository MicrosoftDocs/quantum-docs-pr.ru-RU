---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: Операция Компареусингрипплекарри
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: e2d6e5a663f8c4e101c7e2ab1346d10cade3f4e0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223465"
---
# <a name="compareusingripplecarry-operation"></a><span data-ttu-id="bcf96-102">Операция Компареусингрипплекарри</span><span class="sxs-lookup"><span data-stu-id="bcf96-102">CompareUsingRippleCarry operation</span></span>

<span data-ttu-id="bcf96-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="bcf96-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="bcf96-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bcf96-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bcf96-105">Эта операция проверяет, имеет ли целое число, представленное регистром Кубитс, больше другого целого числа, применяя XOR результата к выходному кубит.</span><span class="sxs-lookup"><span data-stu-id="bcf96-105">This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.</span></span>

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="bcf96-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bcf96-106">Description</span></span>

<span data-ttu-id="bcf96-107">При наличии двух целых чисел `x` и `y` хранении в регистрах кубит одинакового размера эта операция проверяет, соответствуют ли они `x > y` .</span><span class="sxs-lookup"><span data-stu-id="bcf96-107">Given two integers `x` and `y` stored in equal-size qubit registers, this operation checks if they satisfy `x > y`.</span></span> <span data-ttu-id="bcf96-108">Если значение равно true, 1 Ксоред в выходной кубит.</span><span class="sxs-lookup"><span data-stu-id="bcf96-108">If true, 1 is XORed into an output qubit.</span></span> <span data-ttu-id="bcf96-109">В противном случае 0 Ксоред в выходной кубит.</span><span class="sxs-lookup"><span data-stu-id="bcf96-109">Otherwise, 0 is XORed into an output qubit.</span></span>
<span data-ttu-id="bcf96-110">Иными словами, эта операция может быть представлена единой $ $ \бегин{алигн} У\кет {x} \ Сисакет {y} \ Сисакет {z} = \кет{КС}\кет{и}\кет{з\оплус (x>y)}.</span><span class="sxs-lookup"><span data-stu-id="bcf96-110">In other words, this operation can be represented by the unitary $$ \begin{align} U\ket{x}\ket{y}\ket{z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}.</span></span>
<span data-ttu-id="bcf96-111">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="bcf96-111">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="bcf96-112">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bcf96-112">Input</span></span>

### <a name="x--littleendian"></a><span data-ttu-id="bcf96-113">x: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="bcf96-113">x : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="bcf96-114">Первое число для сравнения, хранимое в `LittleEndian` формате в регистре кубит.</span><span class="sxs-lookup"><span data-stu-id="bcf96-114">First number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="y--littleendian"></a><span data-ttu-id="bcf96-115">Да: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="bcf96-115">y : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="bcf96-116">Второе число для сравнения, сохраненное в `LittleEndian` формате в регистре кубит.</span><span class="sxs-lookup"><span data-stu-id="bcf96-116">Second number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="output--qubit"></a><span data-ttu-id="bcf96-117">выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bcf96-117">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="bcf96-118">Кубит, в котором хранится результат сравнения $x>y $.</span><span class="sxs-lookup"><span data-stu-id="bcf96-118">Qubit that stores the result of the comparison $x>y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bcf96-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bcf96-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="bcf96-120">Ссылки</span><span class="sxs-lookup"><span data-stu-id="bcf96-120">References</span></span>

- <span data-ttu-id="bcf96-121">Новый такт Ripple — Добавление Андрея A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон https://arxiv.org/abs/quant-ph/0410184</span><span class="sxs-lookup"><span data-stu-id="bcf96-121">A new quantum ripple-carry addition circuit Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184</span></span>