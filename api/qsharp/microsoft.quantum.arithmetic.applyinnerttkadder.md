---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdder
title: Операция Апплиннертткаддер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdder
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 23c1f6dcdf3894cf1b416efd922c9eed01ac8f85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731873"
---
# <a name="applyinnerttkadder-operation"></a><span data-ttu-id="3a5ed-102">Операция Апплиннертткаддер</span><span class="sxs-lookup"><span data-stu-id="3a5ed-102">ApplyInnerTTKAdder operation</span></span>

<span data-ttu-id="3a5ed-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3a5ed-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3a5ed-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3a5ed-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3a5ed-105">Реализует функцию внутреннего сложения для операции Рипплекарряддерттк.</span><span class="sxs-lookup"><span data-stu-id="3a5ed-105">Implements the inner addition function for the operation RippleCarryAdderTTK.</span></span> <span data-ttu-id="3a5ed-106">Это внутренняя операция, которая сопряжена с внешней операцией для создания полной Adder.</span><span class="sxs-lookup"><span data-stu-id="3a5ed-106">This is the inner operation that is conjugated with the outer operation to construct the full adder.</span></span>

```qsharp
operation ApplyInnerTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="3a5ed-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3a5ed-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="3a5ed-108">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3a5ed-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3a5ed-109">Литтлиндиан кубит Зарегистрируйте первый целочисленный вход слагаемому в Рипплекарряддерттк.</span><span class="sxs-lookup"><span data-stu-id="3a5ed-109">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="3a5ed-110">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3a5ed-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3a5ed-111">Литтлиндиан кубит регистрирует второе целое число входных слагаемому в Рипплекарряддерттк.</span><span class="sxs-lookup"><span data-stu-id="3a5ed-111">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="3a5ed-112">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3a5ed-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3a5ed-113">Кубит, ксоред с наиболее значащим битом суммы.</span><span class="sxs-lookup"><span data-stu-id="3a5ed-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3a5ed-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3a5ed-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3a5ed-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="3a5ed-115">Remarks</span></span>

<span data-ttu-id="3a5ed-116">Указанная управляемая операция использует симметрию и взаимную отмену операций для улучшения реализации по умолчанию, добавляющей элемент управления в каждую операцию.</span><span class="sxs-lookup"><span data-stu-id="3a5ed-116">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="3a5ed-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="3a5ed-117">References</span></span>

- <span data-ttu-id="3a5ed-118">Ясухиро Такахаши, Сеиичиро Тани, Нобору Кунихиро: "каналы добавления тактов и неограниченный вентилятор", сведения о такте и вычисление, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="3a5ed-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530