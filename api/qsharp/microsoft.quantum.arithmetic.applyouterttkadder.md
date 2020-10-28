---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterTTKAdder
title: Операция Апплйоутертткаддер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterTTKAdder
qsharp.summary: Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.
ms.openlocfilehash: 3d6d7c3446075130e5a8ee93abbd27e617d50b3b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731809"
---
# <a name="applyouterttkadder-operation"></a><span data-ttu-id="372b6-102">Операция Апплйоутертткаддер</span><span class="sxs-lookup"><span data-stu-id="372b6-102">ApplyOuterTTKAdder operation</span></span>

<span data-ttu-id="372b6-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="372b6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="372b6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="372b6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="372b6-105">Реализует внешнюю операцию для Рипплекарряддерттк для сопряжения внутренней операции с построением полного Adder.</span><span class="sxs-lookup"><span data-stu-id="372b6-105">Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.</span></span>

```qsharp
operation ApplyOuterTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="372b6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="372b6-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="372b6-107">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="372b6-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="372b6-108">Литтлиндиан кубит Зарегистрируйте первый целочисленный вход слагаемому в Рипплекарряддерттк.</span><span class="sxs-lookup"><span data-stu-id="372b6-108">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="372b6-109">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="372b6-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="372b6-110">Литтлиндиан кубит регистрирует второе целое число входных слагаемому в Рипплекарряддерттк.</span><span class="sxs-lookup"><span data-stu-id="372b6-110">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="372b6-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="372b6-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="372b6-112">Ссылки</span><span class="sxs-lookup"><span data-stu-id="372b6-112">References</span></span>

- <span data-ttu-id="372b6-113">Ясухиро Такахаши, Сеиичиро Тани, Нобору Кунихиро: "каналы добавления тактов и неограниченный вентилятор", сведения о такте и вычисление, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="372b6-113">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530