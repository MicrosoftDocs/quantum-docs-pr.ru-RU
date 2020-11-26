---
uid: Microsoft.Quantum.Arithmetic.GreaterThan
title: Операция GreaterThan
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: GreaterThan
qsharp.summary: Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.
ms.openlocfilehash: 644d68affbdb508938f76de5025a1a463e7284e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223091"
---
# <a name="greaterthan-operation"></a><span data-ttu-id="e8813-102">Операция GreaterThan</span><span class="sxs-lookup"><span data-stu-id="e8813-102">GreaterThan operation</span></span>

<span data-ttu-id="e8813-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e8813-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e8813-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8813-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8813-105">Применяет сравнение типа "больше" между двумя целыми числами, закодированными в регистры кубит, зеркальное отображение целевого кубит на основе результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="e8813-105">Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.</span></span>

```qsharp
operation GreaterThan (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="e8813-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e8813-106">Description</span></span>

<span data-ttu-id="e8813-107">Выполняет строго больше сравнений двух целых чисел $x $ и $y $, закодированных в кубит регистры XS и ИС.</span><span class="sxs-lookup"><span data-stu-id="e8813-107">Carries out a strictly greater than comparison of two integers $x$ and $y$, encoded in qubit registers xs and ys.</span></span> <span data-ttu-id="e8813-108">Если $x > y $, результат будет отражен кубит, в противном случае результат кубит будет оставаться в прежнем состоянии.</span><span class="sxs-lookup"><span data-stu-id="e8813-108">If $x > y$, then the result qubit will be flipped, otherwise the result qubit will retain its state.</span></span>

## <a name="input"></a><span data-ttu-id="e8813-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e8813-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="e8813-110">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e8813-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e8813-111">Литтлиндиан кубит закодировать первое целое число $x $.</span><span class="sxs-lookup"><span data-stu-id="e8813-111">LittleEndian qubit register encoding the first integer $x$.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="e8813-112">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e8813-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e8813-113">Литтлиндиан кубит зарегистрировать второе целое число $y $.</span><span class="sxs-lookup"><span data-stu-id="e8813-113">LittleEndian qubit register encoding the second integer $y$.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="e8813-114">результат: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e8813-114">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e8813-115">Один кубит, который будет отражен, если $x > y $.</span><span class="sxs-lookup"><span data-stu-id="e8813-115">Single qubit that will be flipped if $x > y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e8813-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8813-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e8813-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8813-117">Remarks</span></span>

<span data-ttu-id="e8813-118">Использует прием, который $x-y = (x "+ y)" $, где "обозначает дополнение одного.</span><span class="sxs-lookup"><span data-stu-id="e8813-118">Uses the trick that $x - y = (x'+y)'$, where ' denotes the one's complement.</span></span>

## <a name="references"></a><span data-ttu-id="e8813-119">Ссылки</span><span class="sxs-lookup"><span data-stu-id="e8813-119">References</span></span>

- <span data-ttu-id="e8813-120">Андрей A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон: "Новая тактовая цепь Ripple — комплексное сложение", 2004.</span><span class="sxs-lookup"><span data-stu-id="e8813-120">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1

- <span data-ttu-id="e8813-121">Томас Хаенер, Мартен Роеттелер, Криста M. Своре: "факторинг с использованием 2N + 2 Кубитс с модульным умножением на основе Тоффоли", 2016 https://arxiv.org/abs/1611.07995</span><span class="sxs-lookup"><span data-stu-id="e8813-121">Thomas Haener, Martin Roetteler, Krysta M. Svore: "Factoring using 2n+2 qubits with Toffoli based modular multiplication", 2016 https://arxiv.org/abs/1611.07995</span></span>