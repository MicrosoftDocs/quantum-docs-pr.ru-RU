---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Функция Декомпоседон
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: fb7aa5af8f3eb07399e0d2dd2d50723f4e6b169a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855532"
---
# <a name="decomposedon-function"></a><span data-ttu-id="807d8-102">Функция Декомпоседон</span><span class="sxs-lookup"><span data-stu-id="807d8-102">DecomposedOn function</span></span>

<span data-ttu-id="807d8-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="807d8-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="807d8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="807d8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="807d8-105">Разделяет перестановку на переменную</span><span class="sxs-lookup"><span data-stu-id="807d8-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="807d8-106">Описание</span><span class="sxs-lookup"><span data-stu-id="807d8-106">Description</span></span>

<span data-ttu-id="807d8-107">Учитывая перестановку $ \пи $ ( `perm` ) и индекс $i $ ( `index` ), этот метод возвращает три перестановки $ ((\ pi_l, \ pi_r), \пи ") $ таким, что изображения $ \ pi_l $ и $ \ pi_r $ не изменяют биты в своих элементах в индексах, отличных от $i $ и изображений $ \пи" $ не меняйте бит $i $ в своих элементах.</span><span class="sxs-lookup"><span data-stu-id="807d8-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="807d8-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="807d8-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="807d8-109">разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="807d8-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="807d8-110">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="807d8-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="807d8-111">Выходные данные: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="807d8-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>



## <a name="example"></a><span data-ttu-id="807d8-112">Пример</span><span class="sxs-lookup"><span data-stu-id="807d8-112">Example</span></span>

<span data-ttu-id="807d8-113">Предположим, что входные данные имеют разрешение = [0, 2, 3, 5, 7, 1, 4, 6] и index = 0, а эта функция выполняет три перестановки на основе следующей таблицы, которая перечисляет перестановки `perm` в двоичной нотации элементами в группе A и изображениях в группе D.  В столбцах перечислены битовые индексы.</span><span class="sxs-lookup"><span data-stu-id="807d8-113">Assume that the input is perm = [0, 2, 3, 5, 7, 1, 4, 6] and index = 0, then this function computes three permutations based on the following table, which lists the permutation `perm` in binary notation with elements in group A and images in group D.  The columns list the bit indices.</span></span>

<span data-ttu-id="807d8-114">|   A |   Б |   C |   Г |</span><span class="sxs-lookup"><span data-stu-id="807d8-114">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="807d8-115">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-115">2 1 0</span></span> | <span data-ttu-id="807d8-116">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-116">2 1 0</span></span> | <span data-ttu-id="807d8-117">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-117">2 1 0</span></span> | <span data-ttu-id="807d8-118">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-118">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="807d8-119">0 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-119">0 0 0</span></span> |       |       | <span data-ttu-id="807d8-120">0 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-120">0 0 0</span></span> | <span data-ttu-id="807d8-121">0</span><span class="sxs-lookup"><span data-stu-id="807d8-121">0</span></span>
| <span data-ttu-id="807d8-122">0 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-122">0 0 1</span></span> |       |       | <span data-ttu-id="807d8-123">0 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-123">0 1 0</span></span> | <span data-ttu-id="807d8-124">2</span><span class="sxs-lookup"><span data-stu-id="807d8-124">2</span></span>
| <span data-ttu-id="807d8-125">0 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-125">0 1 0</span></span> |       |       | <span data-ttu-id="807d8-126">0 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-126">0 1 1</span></span> | <span data-ttu-id="807d8-127">3</span><span class="sxs-lookup"><span data-stu-id="807d8-127">3</span></span>
| <span data-ttu-id="807d8-128">0 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-128">0 1 1</span></span> |       |       | <span data-ttu-id="807d8-129">1 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-129">1 0 1</span></span> | <span data-ttu-id="807d8-130">5</span><span class="sxs-lookup"><span data-stu-id="807d8-130">5</span></span>
| <span data-ttu-id="807d8-131">1 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-131">1 0 0</span></span> |       |       | <span data-ttu-id="807d8-132">1 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-132">1 1 1</span></span> | <span data-ttu-id="807d8-133">7</span><span class="sxs-lookup"><span data-stu-id="807d8-133">7</span></span>
| <span data-ttu-id="807d8-134">1 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-134">1 0 1</span></span> |       |       | <span data-ttu-id="807d8-135">0 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-135">0 0 1</span></span> | <span data-ttu-id="807d8-136">1</span><span class="sxs-lookup"><span data-stu-id="807d8-136">1</span></span>
| <span data-ttu-id="807d8-137">1 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-137">1 1 0</span></span> |       |       | <span data-ttu-id="807d8-138">1 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-138">1 0 0</span></span> | <span data-ttu-id="807d8-139">4</span><span class="sxs-lookup"><span data-stu-id="807d8-139">4</span></span>
| <span data-ttu-id="807d8-140">1 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-140">1 1 1</span></span> |       |       | <span data-ttu-id="807d8-141">1 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-141">1 1 0</span></span> | <span data-ttu-id="807d8-142">6</span><span class="sxs-lookup"><span data-stu-id="807d8-142">6</span></span>

<span data-ttu-id="807d8-143">Все значения индексов, не равные 0 (= index), копируются из A в B и с D на C.</span><span class="sxs-lookup"><span data-stu-id="807d8-143">All values for indices not equal to 0 (= index) are copied from A to B and from D to C.</span></span>

<span data-ttu-id="807d8-144">|   A |   Б |   C |   Г |</span><span class="sxs-lookup"><span data-stu-id="807d8-144">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="807d8-145">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-145">2 1 0</span></span> | <span data-ttu-id="807d8-146">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-146">2 1 0</span></span> | <span data-ttu-id="807d8-147">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-147">2 1 0</span></span> | <span data-ttu-id="807d8-148">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-148">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="807d8-149">0 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-149">0 0 0</span></span> | <span data-ttu-id="807d8-150">0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-150">0 0</span></span>   | <span data-ttu-id="807d8-151">0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-151">0 0</span></span>   | <span data-ttu-id="807d8-152">0 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-152">0 0 0</span></span> |
| <span data-ttu-id="807d8-153">0 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-153">0 0 1</span></span> | <span data-ttu-id="807d8-154">0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-154">0 0</span></span>   | <span data-ttu-id="807d8-155">0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-155">0 1</span></span>   | <span data-ttu-id="807d8-156">0 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-156">0 1 0</span></span> |
| <span data-ttu-id="807d8-157">0 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-157">0 1 0</span></span> | <span data-ttu-id="807d8-158">0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-158">0 1</span></span>   | <span data-ttu-id="807d8-159">0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-159">0 1</span></span>   | <span data-ttu-id="807d8-160">0 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-160">0 1 1</span></span> |
| <span data-ttu-id="807d8-161">0 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-161">0 1 1</span></span> | <span data-ttu-id="807d8-162">0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-162">0 1</span></span>   | <span data-ttu-id="807d8-163">1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-163">1 0</span></span>   | <span data-ttu-id="807d8-164">1 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-164">1 0 1</span></span> |
| <span data-ttu-id="807d8-165">1 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-165">1 0 0</span></span> | <span data-ttu-id="807d8-166">1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-166">1 0</span></span>   | <span data-ttu-id="807d8-167">1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-167">1 1</span></span>   | <span data-ttu-id="807d8-168">1 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-168">1 1 1</span></span> |
| <span data-ttu-id="807d8-169">1 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-169">1 0 1</span></span> | <span data-ttu-id="807d8-170">1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-170">1 0</span></span>   | <span data-ttu-id="807d8-171">0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-171">0 0</span></span>   | <span data-ttu-id="807d8-172">0 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-172">0 0 1</span></span> |
| <span data-ttu-id="807d8-173">1 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-173">1 1 0</span></span> | <span data-ttu-id="807d8-174">1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-174">1 1</span></span>   | <span data-ttu-id="807d8-175">1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-175">1 0</span></span>   | <span data-ttu-id="807d8-176">1 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-176">1 0 0</span></span> |
| <span data-ttu-id="807d8-177">1 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-177">1 1 1</span></span> | <span data-ttu-id="807d8-178">1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-178">1 1</span></span>   | <span data-ttu-id="807d8-179">1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-179">1 1</span></span>   | <span data-ttu-id="807d8-180">1 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-180">1 1 0</span></span> |

<span data-ttu-id="807d8-181">Далее 0 размещается для первого элемента с пустым индексом в столбце 0 в блоке B, а затем 1 помещается в B, где префикс совпадает (в первом случае это другая строка с индексами 0 0).</span><span class="sxs-lookup"><span data-stu-id="807d8-181">Next a 0 is placed for the first element with an empty index at column 0 in block B and then a 1 is placed in B where the prefix matches (in the first case the other row with indices 0 0).</span></span>
<span data-ttu-id="807d8-182">Затем 1 добавляется в ту же строку блока C, а затем значение 0 для соответствующего префикса в блоке C.  Этот процесс повторяется, пока все индексы не будут помещены в столбец 0 в блоках B и C.</span><span class="sxs-lookup"><span data-stu-id="807d8-182">Afterwards, a 1 is added in the same row in block C, and then a 0 for the corresponding prefix in block C.  This process is repeated, until all indices have been placed in column 0 in blocks B and C.</span></span>

<span data-ttu-id="807d8-183">|   A |   Б |   C |   Г |</span><span class="sxs-lookup"><span data-stu-id="807d8-183">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="807d8-184">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-184">2 1 0</span></span> | <span data-ttu-id="807d8-185">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-185">2 1 0</span></span> | <span data-ttu-id="807d8-186">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-186">2 1 0</span></span> | <span data-ttu-id="807d8-187">2 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-187">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="807d8-188">0 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-188">0 0 0</span></span> | <span data-ttu-id="807d8-189">0 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-189">0 0 0</span></span> | <span data-ttu-id="807d8-190">0 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-190">0 0 0</span></span> | <span data-ttu-id="807d8-191">0 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-191">0 0 0</span></span> |
| <span data-ttu-id="807d8-192">0 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-192">0 0 1</span></span> | <span data-ttu-id="807d8-193">0 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-193">0 0 1</span></span> | <span data-ttu-id="807d8-194">0 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-194">0 1 1</span></span> | <span data-ttu-id="807d8-195">0 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-195">0 1 0</span></span> |
| <span data-ttu-id="807d8-196">0 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-196">0 1 0</span></span> | <span data-ttu-id="807d8-197">0 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-197">0 1 0</span></span> | <span data-ttu-id="807d8-198">0 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-198">0 1 0</span></span> | <span data-ttu-id="807d8-199">0 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-199">0 1 1</span></span> |
| <span data-ttu-id="807d8-200">0 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-200">0 1 1</span></span> | <span data-ttu-id="807d8-201">0 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-201">0 1 1</span></span> | <span data-ttu-id="807d8-202">1 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-202">1 0 1</span></span> | <span data-ttu-id="807d8-203">1 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-203">1 0 1</span></span> |
| <span data-ttu-id="807d8-204">1 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-204">1 0 0</span></span> | <span data-ttu-id="807d8-205">1 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-205">1 0 0</span></span> | <span data-ttu-id="807d8-206">1 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-206">1 1 0</span></span> | <span data-ttu-id="807d8-207">1 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-207">1 1 1</span></span> |
| <span data-ttu-id="807d8-208">1 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-208">1 0 1</span></span> | <span data-ttu-id="807d8-209">1 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-209">1 0 1</span></span> | <span data-ttu-id="807d8-210">0 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-210">0 0 1</span></span> | <span data-ttu-id="807d8-211">0 0 1</span><span class="sxs-lookup"><span data-stu-id="807d8-211">0 0 1</span></span> |
| <span data-ttu-id="807d8-212">1 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-212">1 1 0</span></span> | <span data-ttu-id="807d8-213">1 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-213">1 1 0</span></span> | <span data-ttu-id="807d8-214">1 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-214">1 0 0</span></span> | <span data-ttu-id="807d8-215">1 0 0</span><span class="sxs-lookup"><span data-stu-id="807d8-215">1 0 0</span></span> |
| <span data-ttu-id="807d8-216">1 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-216">1 1 1</span></span> | <span data-ttu-id="807d8-217">1 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-217">1 1 1</span></span> | <span data-ttu-id="807d8-218">1 1 1</span><span class="sxs-lookup"><span data-stu-id="807d8-218">1 1 1</span></span> | <span data-ttu-id="807d8-219">1 1 0</span><span class="sxs-lookup"><span data-stu-id="807d8-219">1 1 0</span></span> |

<span data-ttu-id="807d8-220">В таблице можно прочитать три новые перестановки:</span><span class="sxs-lookup"><span data-stu-id="807d8-220">We can read three new permutations from the table:</span></span>

- <span data-ttu-id="807d8-221">$ \ pi_l $ с элементами в, изображения в B (слева)</span><span class="sxs-lookup"><span data-stu-id="807d8-221">$\pi_l$ with elements in A, images in B (left)</span></span>
- <span data-ttu-id="807d8-222">$ \ pi_r $ с элементами в D, изображения в C (справа)</span><span class="sxs-lookup"><span data-stu-id="807d8-222">$\pi_r$ with elements in D, images in C (right)</span></span>
- <span data-ttu-id="807d8-223">$ \пи ' $ с элементами в B, изображения в C (остаток)</span><span class="sxs-lookup"><span data-stu-id="807d8-223">$\pi'$  with elements in B, images in C (remainder)</span></span>

<span data-ttu-id="807d8-224">Обратите внимание на то, что значения битов проектирования не изменяются в $ \ pi_l $ и $ \ pi_r $ для индексов 1 и 2, а битовые значения не изменяются для in $ \ pi_ ' $ для индекса 0.</span><span class="sxs-lookup"><span data-stu-id="807d8-224">Note that by design bit values do not change in $\pi_l$ and $\pi_r$ for indices 1 and 2, and bit values do not change for in $\pi_'$ for index 0.</span></span>  <span data-ttu-id="807d8-225">Также обратите внимание, что $ \ pi_l $ и $ \ pi_r $ должны быть самообратными.</span><span class="sxs-lookup"><span data-stu-id="807d8-225">Also note that $\pi_l$ and $\pi_r$ must be self-inverse.</span></span>

<span data-ttu-id="807d8-226">Наследуемые и возвращаемые перестановки: Left = [0, 1, 2, 3, 4, 5, 6, 7] право = [0, 1, 3, 2, 4, 5, 7, 6] остаток = [0, 3, 2, 5, 6, 1, 4, 7]</span><span class="sxs-lookup"><span data-stu-id="807d8-226">The derived and returned permutations are: left      = [0, 1, 2, 3, 4, 5, 6, 7] right     = [0, 1, 3, 2, 4, 5, 7, 6] remainder = [0, 3, 2, 5, 6, 1, 4, 7]</span></span>