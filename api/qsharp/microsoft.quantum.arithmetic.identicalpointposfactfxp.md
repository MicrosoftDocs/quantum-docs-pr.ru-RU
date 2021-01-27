---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: Функция Идентикалпоинтпосфактфксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 7212f918e1d0ee86b12b85caa6e0c27bc2cebe58
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846621"
---
# <a name="identicalpointposfactfxp-function"></a><span data-ttu-id="0a4d1-102">Функция Идентикалпоинтпосфактфксп</span><span class="sxs-lookup"><span data-stu-id="0a4d1-102">IdenticalPointPosFactFxP function</span></span>

<span data-ttu-id="0a4d1-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0a4d1-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0a4d1-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="0a4d1-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="0a4d1-105">Утверждает, что все числа с фиксированной запятой в предоставленном массиве имеют одинаковые позиции точек при подсчете из наименьшего значащих битов.</span><span class="sxs-lookup"><span data-stu-id="0a4d1-105">Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit.</span></span> <span data-ttu-id="0a4d1-106">Т. е. количество битов минус позиции точки должно быть константой для всех чисел с фиксированной запятой в массиве.</span><span class="sxs-lookup"><span data-stu-id="0a4d1-106">I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.</span></span>

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a><span data-ttu-id="0a4d1-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0a4d1-107">Input</span></span>

### <a name="fixedpoints--fixedpoint"></a><span data-ttu-id="0a4d1-108">Фикседпоинтс: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span><span class="sxs-lookup"><span data-stu-id="0a4d1-108">fixedPoints : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span></span>

<span data-ttu-id="0a4d1-109">Массив чисел с фиксированной запятой, которые будут проверяться на совместимость (с помощью утверждений).</span><span class="sxs-lookup"><span data-stu-id="0a4d1-109">Array of quantum fixed-point numbers that will be checked for compatibility (using assertions).</span></span>



## <a name="output--unit"></a><span data-ttu-id="0a4d1-110">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0a4d1-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

