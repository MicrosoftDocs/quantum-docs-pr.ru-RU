---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: Операция Аддфксп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: cf1f1379b7e1c32aefb0fccb55f4d13c95c78d8f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731904"
---
# <a name="addfxp-operation"></a><span data-ttu-id="0063d-102">Операция Аддфксп</span><span class="sxs-lookup"><span data-stu-id="0063d-102">AddFxP operation</span></span>

<span data-ttu-id="0063d-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0063d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0063d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0063d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0063d-105">Добавляет два числа с фиксированной запятой, хранящихся в тактовых регистрах.</span><span class="sxs-lookup"><span data-stu-id="0063d-105">Adds two fixed-point numbers stored in quantum registers.</span></span>

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="description"></a><span data-ttu-id="0063d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0063d-106">Description</span></span>

<span data-ttu-id="0063d-107">При наличии двух регистров с фиксированной запятой соответственно в состояниях $ \кет{f_1} $ и $ \кет{f_2} $ выполняет операцию $ \кет{f_1} \кет{f_2} \мапсто \кет{f_1} \кет{f_1 + f_2} $.</span><span class="sxs-lookup"><span data-stu-id="0063d-107">Given two fixed-point registers respectively in states $\ket{f_1}$ and $\ket{f_2}$, performs the operation $\ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2}$.</span></span>

## <a name="input"></a><span data-ttu-id="0063d-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0063d-108">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="0063d-109">FP1: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="0063d-109">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="0063d-110">Первое число с фиксированной запятой</span><span class="sxs-lookup"><span data-stu-id="0063d-110">First fixed-point number</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="0063d-111">Fp2: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="0063d-111">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="0063d-112">Второе число с фиксированной запятой будет обновлено для включения суммы двух входных значений.</span><span class="sxs-lookup"><span data-stu-id="0063d-112">Second fixed-point number, will be updated to contain the sum of the two inputs.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0063d-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0063d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="0063d-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="0063d-114">Remarks</span></span>

<span data-ttu-id="0063d-115">Для текущей реализации требуется, чтобы два числа с фиксированной запятой имели одинаковую позицию точки с наименьшего значащим битом, т. е. $n _i $ и $p _i $ должны быть равны.</span><span class="sxs-lookup"><span data-stu-id="0063d-115">The current implementation requires the two fixed-point numbers to have the same point position counting from the least-significant bit, i.e., $n_i$ and $p_i$ must be equal.</span></span>