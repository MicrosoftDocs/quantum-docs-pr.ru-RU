---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: Операция Аддфксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: 60b7cad3d0bd8800e67830ca921f8e2d705b8f39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843859"
---
# <a name="addfxp-operation"></a><span data-ttu-id="98a9a-102">Операция Аддфксп</span><span class="sxs-lookup"><span data-stu-id="98a9a-102">AddFxP operation</span></span>

<span data-ttu-id="98a9a-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="98a9a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="98a9a-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="98a9a-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="98a9a-105">Добавляет два числа с фиксированной запятой, хранящихся в тактовых регистрах.</span><span class="sxs-lookup"><span data-stu-id="98a9a-105">Adds two fixed-point numbers stored in quantum registers.</span></span>

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="98a9a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="98a9a-106">Description</span></span>

<span data-ttu-id="98a9a-107">При наличии двух регистров с фиксированной запятой соответственно в состояниях $ \кет{f_1} $ и $ \кет{f_2} $ выполняет операцию $ \кет{f_1} \кет{f_2} \мапсто \кет{f_1} \кет{f_1 + f_2} $.</span><span class="sxs-lookup"><span data-stu-id="98a9a-107">Given two fixed-point registers respectively in states $\ket{f_1}$ and $\ket{f_2}$, performs the operation $\ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2}$.</span></span>

## <a name="input"></a><span data-ttu-id="98a9a-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="98a9a-108">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="98a9a-109">FP1: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="98a9a-109">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="98a9a-110">Первое число с фиксированной запятой</span><span class="sxs-lookup"><span data-stu-id="98a9a-110">First fixed-point number</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="98a9a-111">Fp2: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="98a9a-111">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="98a9a-112">Второе число с фиксированной запятой будет обновлено для включения суммы двух входных значений.</span><span class="sxs-lookup"><span data-stu-id="98a9a-112">Second fixed-point number, will be updated to contain the sum of the two inputs.</span></span>



## <a name="output--unit"></a><span data-ttu-id="98a9a-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="98a9a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="98a9a-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="98a9a-114">Remarks</span></span>

<span data-ttu-id="98a9a-115">Для текущей реализации требуется, чтобы два числа с фиксированной запятой имели одинаковую позицию точки с наименьшего значащим битом, т. е. $n _i $ и $p _i $ должны быть равны.</span><span class="sxs-lookup"><span data-stu-id="98a9a-115">The current implementation requires the two fixed-point numbers to have the same point position counting from the least-significant bit, i.e., $n_i$ and $p_i$ must be equal.</span></span>