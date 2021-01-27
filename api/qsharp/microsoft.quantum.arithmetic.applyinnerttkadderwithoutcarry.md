---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdderWithoutCarry
title: Операция Апплиннертткаддервисауткарри
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdderWithoutCarry
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 0c1626c788215181b5ed45dc98bed928b5e4848a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843808"
---
# <a name="applyinnerttkadderwithoutcarry-operation"></a><span data-ttu-id="e956f-102">Операция Апплиннертткаддервисауткарри</span><span class="sxs-lookup"><span data-stu-id="e956f-102">ApplyInnerTTKAdderWithoutCarry operation</span></span>

<span data-ttu-id="e956f-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e956f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e956f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e956f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e956f-105">Реализует функцию внутреннего сложения для операции Рипплекарряддернокарриттк.</span><span class="sxs-lookup"><span data-stu-id="e956f-105">Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK.</span></span> <span data-ttu-id="e956f-106">Это внутренняя операция, которая сопряжена с внешней операцией для создания полной Adder.</span><span class="sxs-lookup"><span data-stu-id="e956f-106">This is the inner operation that is conjugated with the outer operation to construct the full adder.</span></span>

```qsharp
operation ApplyInnerTTKAdderWithoutCarry (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e956f-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e956f-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="e956f-108">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e956f-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e956f-109">Литтлиндиан кубит Зарегистрируйте первый целочисленный вход слагаемому в Рипплекарряддернокарриттк.</span><span class="sxs-lookup"><span data-stu-id="e956f-109">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderNoCarryTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="e956f-110">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e956f-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e956f-111">Литтлиндиан кубит регистрирует второе целое число входных слагаемому в Рипплекарряддернокарриттк.</span><span class="sxs-lookup"><span data-stu-id="e956f-111">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderNoCarryTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e956f-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e956f-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e956f-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="e956f-113">Remarks</span></span>

<span data-ttu-id="e956f-114">Указанная управляемая операция использует симметрию и взаимную отмену операций для улучшения реализации по умолчанию, добавляющей элемент управления в каждую операцию.</span><span class="sxs-lookup"><span data-stu-id="e956f-114">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="e956f-115">Ссылки</span><span class="sxs-lookup"><span data-stu-id="e956f-115">References</span></span>

- <span data-ttu-id="e956f-116">Ясухиро Такахаши, Сеиичиро Тани, Нобору Кунихиро: "каналы добавления тактов и неограниченный вентилятор", сведения о такте и вычисление, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="e956f-116">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530