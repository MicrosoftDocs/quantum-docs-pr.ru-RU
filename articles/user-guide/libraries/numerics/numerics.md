---
title: Использование библиотеки числовых средств (Майкрософт) Q#
description: Сведения о типах и операциях, доступных в библиотеке цифровых чисел Microsoft тактов.
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: conceptual
uid: microsoft.quantum.numerics.usage
no-loc:
- Q#
- $$v
ms.openlocfilehash: 92efd3b8677d2f27bc59f986ce6c9e915cd23652
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856441"
---
# <a name="using-the-numerics-library"></a><span data-ttu-id="e651a-103">Использование библиотеки числовых средств</span><span class="sxs-lookup"><span data-stu-id="e651a-103">Using the Numerics library</span></span>

## <a name="overview"></a><span data-ttu-id="e651a-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="e651a-104">Overview</span></span>

<span data-ttu-id="e651a-105">Библиотека числовых данных состоит из трех компонентов.</span><span class="sxs-lookup"><span data-stu-id="e651a-105">The Numerics library consists of three components</span></span>

1. <span data-ttu-id="e651a-106">**Базовая целочисленная арифметика** с целочисленным методах и операторами сравнения</span><span class="sxs-lookup"><span data-stu-id="e651a-106">**Basic integer arithmetic** with integer adders and comparators</span></span>
1. <span data-ttu-id="e651a-107">**Высокоуровневые целочисленные функции** , построенные на основе базовой функциональности; Он включает умножение, деление, инверсию и т. д.  для целых чисел со знаком и без знака.</span><span class="sxs-lookup"><span data-stu-id="e651a-107">**High-level integer functionality** that is built on top of the basic  functionality; it includes multiplication, division, inversion, etc.  for signed and unsigned integers.</span></span>
1. <span data-ttu-id="e651a-108">**Арифметические функции с фиксированной запятой** с инициализацией, сложение, умножение, обратная Оценка и измерение.</span><span class="sxs-lookup"><span data-stu-id="e651a-108">**Fixed-point arithmetic functionality** with fixed-point initialization,  addition, multiplication, reciprocal, polynomial evaluation, and measurement.</span></span>

<span data-ttu-id="e651a-109">Доступ ко всем этим компонентам можно получить с помощью одной `open` инструкции:</span><span class="sxs-lookup"><span data-stu-id="e651a-109">All of these components can be accessed using a single `open` statement:</span></span>
```qsharp
open Microsoft.Quantum.Arithmetic;
```

## <a name="types"></a><span data-ttu-id="e651a-110">Типы</span><span class="sxs-lookup"><span data-stu-id="e651a-110">Types</span></span>

<span data-ttu-id="e651a-111">Библиотека числовых типов поддерживает следующие типы</span><span class="sxs-lookup"><span data-stu-id="e651a-111">The numerics library supports the following types</span></span>

1. <span data-ttu-id="e651a-112">**`LittleEndian`**: Массив кубит `qArr : Qubit[]` , представляющий целое число, где `qArr[0]` обозначает наименее значащий бит.</span><span class="sxs-lookup"><span data-stu-id="e651a-112">**`LittleEndian`**: A qubit array `qArr : Qubit[]` that represents an integer where `qArr[0]` denotes the least significant bit.</span></span>
1. <span data-ttu-id="e651a-113">**`SignedLittleEndian`**: То же `LittleEndian` , что и за исключением того, что он представляет целое число со знаком, хранящееся в дополнениех двух.</span><span class="sxs-lookup"><span data-stu-id="e651a-113">**`SignedLittleEndian`**: Same as `LittleEndian` except that it represents a signed integer stored in two's complement.</span></span>
1. <span data-ttu-id="e651a-114">**`FixedPoint`**— Представляет вещественное число, состоящее из массива кубит `qArr2 : Qubit[]` и позиции двоичной точки `pos` , которая подсчитывает количество двоичных разрядов слева от двоичной точки.</span><span class="sxs-lookup"><span data-stu-id="e651a-114">**`FixedPoint`**: Represents a real number consisting of a qubit array `qArr2 : Qubit[]` and a binary point position `pos`, which counts the number of binary digits to the left of the binary point.</span></span> <span data-ttu-id="e651a-115">`qArr2` хранится так же, как и `SignedLittleEndian` .</span><span class="sxs-lookup"><span data-stu-id="e651a-115">`qArr2` is stored in the same way as `SignedLittleEndian`.</span></span>

## <a name="operations"></a><span data-ttu-id="e651a-116">Операции</span><span class="sxs-lookup"><span data-stu-id="e651a-116">Operations</span></span>

<span data-ttu-id="e651a-117">Для каждого из трех перечисленных выше типов доступны различные операции:</span><span class="sxs-lookup"><span data-stu-id="e651a-117">For each of the three types above, a variety of operations is available:</span></span>

1. **`LittleEndian`**
    - <span data-ttu-id="e651a-118">Сложение</span><span class="sxs-lookup"><span data-stu-id="e651a-118">Addition</span></span>
    - <span data-ttu-id="e651a-119">Сравнение</span><span class="sxs-lookup"><span data-stu-id="e651a-119">Comparison</span></span>
    - <span data-ttu-id="e651a-120">Умножение</span><span class="sxs-lookup"><span data-stu-id="e651a-120">Multiplication</span></span>
    - <span data-ttu-id="e651a-121">Ведения</span><span class="sxs-lookup"><span data-stu-id="e651a-121">Squaring</span></span>
    - <span data-ttu-id="e651a-122">Деление (с остатком)</span><span class="sxs-lookup"><span data-stu-id="e651a-122">Division (with remainder)</span></span>

1. **`SignedLittleEndian`**
    - <span data-ttu-id="e651a-123">Сложение</span><span class="sxs-lookup"><span data-stu-id="e651a-123">Addition</span></span>
    - <span data-ttu-id="e651a-124">Сравнение</span><span class="sxs-lookup"><span data-stu-id="e651a-124">Comparison</span></span>
    - <span data-ttu-id="e651a-125">Дополнение модуля инверсии по модулю 2</span><span class="sxs-lookup"><span data-stu-id="e651a-125">Inversion modulo 2's complement</span></span>
    - <span data-ttu-id="e651a-126">Умножение</span><span class="sxs-lookup"><span data-stu-id="e651a-126">Multiplication</span></span>
    - <span data-ttu-id="e651a-127">Ведения</span><span class="sxs-lookup"><span data-stu-id="e651a-127">Squaring</span></span>

1. **`FixedPoint`**
    - <span data-ttu-id="e651a-128">Подготовка или инициализация для классических значений</span><span class="sxs-lookup"><span data-stu-id="e651a-128">Preparation / initialization to a classical values</span></span>
    - <span data-ttu-id="e651a-129">Сложение (классическая константа или другой такт с фиксированной точкой)</span><span class="sxs-lookup"><span data-stu-id="e651a-129">Addition (classical constant or other quantum fixed-point)</span></span>
    - <span data-ttu-id="e651a-130">Сравнение</span><span class="sxs-lookup"><span data-stu-id="e651a-130">Comparison</span></span>
    - <span data-ttu-id="e651a-131">Умножение</span><span class="sxs-lookup"><span data-stu-id="e651a-131">Multiplication</span></span>
    - <span data-ttu-id="e651a-132">Ведения</span><span class="sxs-lookup"><span data-stu-id="e651a-132">Squaring</span></span>
    - <span data-ttu-id="e651a-133">Оценка полинома с специализацией для четных и нечетных функций</span><span class="sxs-lookup"><span data-stu-id="e651a-133">Polynomial evaluation with specialization for even and odd functions</span></span>
    - <span data-ttu-id="e651a-134">Обратная (1/x)</span><span class="sxs-lookup"><span data-stu-id="e651a-134">Reciprocal (1/x)</span></span>
    - <span data-ttu-id="e651a-135">Измерение (классическое значение Double)</span><span class="sxs-lookup"><span data-stu-id="e651a-135">Measurement (classical Double)</span></span>

<span data-ttu-id="e651a-136">Дополнительные сведения и подробную документацию по каждой из этих операций см. в Q# справочной документации по библиотеке по адресу [docs.Microsoft.com](https://docs.microsoft.com/quantum)</span><span class="sxs-lookup"><span data-stu-id="e651a-136">For more information and detailed documentation for each of these operations, see the Q# library reference docs at [docs.microsoft.com](https://docs.microsoft.com/quantum)</span></span>

## <a name="sample-integer-addition"></a><span data-ttu-id="e651a-137">Пример: сложение целых чисел</span><span class="sxs-lookup"><span data-stu-id="e651a-137">Sample: Integer addition</span></span>

<span data-ttu-id="e651a-138">В качестве простого примера рассмотрим операцию $ $ \кет кс\кет и\мапсто \кет кс\кет {x + y} $ $, т. е. операцию, которая принимает n-кубит целое $x $ и n-или (n + 1)-кубит Register $y $ в качестве входных данных, второй из которых сопоставляется с суммой $ (x + y) $.</span><span class="sxs-lookup"><span data-stu-id="e651a-138">As a basic example, consider the operation $$ \ket x\ket y\mapsto \ket x\ket{x+y} $$ that is, an operation that takes an n-qubit integer $x$ and an n- or (n+1)-qubit register $y$ as input, the latter of which it maps to the sum $(x+y)$.</span></span> <span data-ttu-id="e651a-139">Обратите внимание, что сумма вычисляется по модулю $2 ^ n $, если $y $ хранится в $n $-разрядном регистре.</span><span class="sxs-lookup"><span data-stu-id="e651a-139">Note that the sum is computed modulo $2^n$ if $y$ is stored in an $n$-bit register.</span></span>

<span data-ttu-id="e651a-140">С помощью пакета средств разработки тактов эту операцию можно применить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e651a-140">Using the Quantum Development Kit, this operation can be applied as follows:</span></span>
```qsharp
operation TestMyAddition(xValue : Int, yValue : Int, n : Int) : Unit {
    using ((xQubits, yQubits) = (Qubit[n], Qubit[n]))
    {
        let x = LittleEndian(xQubits); // define bit order
        let y = LittleEndian(yQubits);
        
        ApplyXorInPlace(xValue, x); // initialize values
        ApplyXorInPlace(yValue, y);
        
        AddI(x, y); // perform addition x+y into y
        
        // ... (use the result)
    }
}
```

## <a name="sample-evaluating-smooth-functions"></a><span data-ttu-id="e651a-141">Пример. Вычисление гладких функций</span><span class="sxs-lookup"><span data-stu-id="e651a-141">Sample: Evaluating smooth functions</span></span>

<span data-ttu-id="e651a-142">Для вычисления гладких функций, таких как $ \син (x) $, на тактовый компьютер, где $x $ — это тактовый `FixedPoint` номер, Библиотека числовых пакетов разработки тактов предоставляет операции `EvaluatePolynomialFxP` и `Evaluate[Even/Odd]PolynomialFxP` .</span><span class="sxs-lookup"><span data-stu-id="e651a-142">To evaluate smooth functions such as $\sin(x)$ on a quantum computer, where $x$ is a quantum `FixedPoint` number, the Quantum Development Kit numerics library provides the operations `EvaluatePolynomialFxP` and `Evaluate[Even/Odd]PolynomialFxP`.</span></span>

<span data-ttu-id="e651a-143">Первый, `EvaluatePolynomialFxP` ,, позволяет оценить полином вида $ $ P (x) = a_0 + a_1x + a_2x ^ 2 + \кдотс + a_dx ^ d, $ $, где $d $ обозначает *степень*.</span><span class="sxs-lookup"><span data-stu-id="e651a-143">The first, `EvaluatePolynomialFxP`, allows to evaluate a polynomial of the form $$ P(x) = a_0 + a_1x + a_2x^2 + \cdots + a_dx^d, $$ where $d$ denotes the *degree*.</span></span> <span data-ttu-id="e651a-144">Для этого все, что требуется, — это коэффициенты полинома `[a_0,..., a_d]` (типа `Double[]` ), входные `x : FixedPoint` и выходные данные `y : FixedPoint` (изначально ноль):</span><span class="sxs-lookup"><span data-stu-id="e651a-144">To do so, all that is needed are the polynomial coefficients `[a_0,..., a_d]` (of type `Double[]`), the input `x : FixedPoint` and the output `y : FixedPoint` (initially zero):</span></span>
```qsharp
EvaluatePolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="e651a-145">Результат, $P (x) = 1 + 2x $, будет сохранен в `yFxP` .</span><span class="sxs-lookup"><span data-stu-id="e651a-145">The result, $P(x)=1+2x$, will be stored in `yFxP`.</span></span>

<span data-ttu-id="e651a-146">Второй, `EvaluateEvenPolynomialFxP` , и третий, `EvaluateOddPolynomialFxP` являются специализациями для случаев четных и нечетных функций соответственно.</span><span class="sxs-lookup"><span data-stu-id="e651a-146">The second, `EvaluateEvenPolynomialFxP`, and the third, `EvaluateOddPolynomialFxP`, are specializations for the cases of even and odd functions, respectively.</span></span> <span data-ttu-id="e651a-147">Это значит, что для четной или нечетной функции $f (x) $ и $ $ P_ {четный} (x) = a_0 + a_1 x ^ 2 + a_2 x ^ 4 + \кдотс + a_d x ^ {2D}, $ $ $f (x) $ приближенно подходит $P _ {четный} (x) $ или $P _ {нечет} (x): = кс\кдот P_ {четный} (x) $ соответственно.</span><span class="sxs-lookup"><span data-stu-id="e651a-147">That is, for an even/odd function $f(x)$ and $$ P_{even}(x)=a_0 + a_1 x^2 + a_2 x^4 + \cdots + a_d x^{2d}, $$ $f(x)$ is approximated well by $P_{even}(x)$ or $P_{odd}(x) := x\cdot P_{even}(x)$, respectively.</span></span>
<span data-ttu-id="e651a-148">В Q# эти два варианта можно обрабатывать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e651a-148">In Q#, these two cases can be handled as follows:</span></span>
```qsharp
EvaluateEvenPolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="e651a-149">который вычисляет $P _ {четный} (x) = 1 + 2x ^ 2 $ и</span><span class="sxs-lookup"><span data-stu-id="e651a-149">which evaluates $P_{even}(x) = 1 + 2x^2$, and</span></span>
```qsharp
EvaluateOddPolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="e651a-150">который вычисляет $P _ {нечетный} (x) = x + 2x ^ 3 $.</span><span class="sxs-lookup"><span data-stu-id="e651a-150">which evaluates $P_{odd}(x) = x + 2x^3$.</span></span>

## <a name="more-samples"></a><span data-ttu-id="e651a-151">Другие примеры</span><span class="sxs-lookup"><span data-stu-id="e651a-151">More samples</span></span>

<span data-ttu-id="e651a-152">Дополнительные примеры можно найти в [основном репозитории примеров](https://github.com/Microsoft/Quantum).</span><span class="sxs-lookup"><span data-stu-id="e651a-152">You can find more samples in the [main samples repository](https://github.com/Microsoft/Quantum).</span></span>

<span data-ttu-id="e651a-153">Чтобы приступить к работе, клонировать репозиторий и открыть `Numerics` вложенную папку:</span><span class="sxs-lookup"><span data-stu-id="e651a-153">To get started, clone the repo and open the `Numerics` subfolder:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics
```

<span data-ttu-id="e651a-154">Затем `cd` в один из примеров папок и запустите пример с помощью</span><span class="sxs-lookup"><span data-stu-id="e651a-154">Then, `cd` into one of the sample folders and run the sample via</span></span>

```bash
dotnet run
```
