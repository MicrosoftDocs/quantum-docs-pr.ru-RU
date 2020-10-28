---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdderWithoutCarry
title: Операция Апплиннертткаддервисауткарри
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdderWithoutCarry
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 3335c63b8509090deed1172419158da0d5e80409
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731865"
---
# <a name="applyinnerttkadderwithoutcarry-operation"></a><span data-ttu-id="85e89-102">Операция Апплиннертткаддервисауткарри</span><span class="sxs-lookup"><span data-stu-id="85e89-102">ApplyInnerTTKAdderWithoutCarry operation</span></span>

<span data-ttu-id="85e89-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="85e89-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="85e89-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="85e89-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="85e89-105">Реализует функцию внутреннего сложения для операции Рипплекарряддернокарриттк.</span><span class="sxs-lookup"><span data-stu-id="85e89-105">Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK.</span></span> <span data-ttu-id="85e89-106">Это внутренняя операция, которая сопряжена с внешней операцией для создания полной Adder.</span><span class="sxs-lookup"><span data-stu-id="85e89-106">This is the inner operation that is conjugated with the outer operation to construct the full adder.</span></span>

```qsharp
operation ApplyInnerTTKAdderWithoutCarry (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="85e89-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="85e89-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="85e89-108">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="85e89-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="85e89-109">Литтлиндиан кубит Зарегистрируйте первый целочисленный вход слагаемому в Рипплекарряддернокарриттк.</span><span class="sxs-lookup"><span data-stu-id="85e89-109">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderNoCarryTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="85e89-110">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="85e89-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="85e89-111">Литтлиндиан кубит регистрирует второе целое число входных слагаемому в Рипплекарряддернокарриттк.</span><span class="sxs-lookup"><span data-stu-id="85e89-111">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderNoCarryTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="85e89-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="85e89-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="85e89-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="85e89-113">Remarks</span></span>

<span data-ttu-id="85e89-114">Указанная управляемая операция использует симметрию и взаимную отмену операций для улучшения реализации по умолчанию, добавляющей элемент управления в каждую операцию.</span><span class="sxs-lookup"><span data-stu-id="85e89-114">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="85e89-115">Ссылки</span><span class="sxs-lookup"><span data-stu-id="85e89-115">References</span></span>

- <span data-ttu-id="85e89-116">Ясухиро Такахаши, Сеиичиро Тани, Нобору Кунихиро: "каналы добавления тактов и неограниченный вентилятор", сведения о такте и вычисление, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="85e89-116">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530