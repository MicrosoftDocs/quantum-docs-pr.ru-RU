---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: Функция Идентикалпоинтпосфактфксп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 0b285ce980ca1abbc3eb20838389a6f49835e742
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731513"
---
# <a name="identicalpointposfactfxp-function"></a><span data-ttu-id="aea40-102">Функция Идентикалпоинтпосфактфксп</span><span class="sxs-lookup"><span data-stu-id="aea40-102">IdenticalPointPosFactFxP function</span></span>

<span data-ttu-id="aea40-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="aea40-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="aea40-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aea40-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aea40-105">Утверждает, что все числа с фиксированной запятой в предоставленном массиве имеют одинаковые позиции точек при подсчете из наименьшего значащих битов.</span><span class="sxs-lookup"><span data-stu-id="aea40-105">Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit.</span></span> <span data-ttu-id="aea40-106">Т. е. количество битов минус позиции точки должно быть константой для всех чисел с фиксированной запятой в массиве.</span><span class="sxs-lookup"><span data-stu-id="aea40-106">I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.</span></span>

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a><span data-ttu-id="aea40-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="aea40-107">Input</span></span>

### <a name="fixedpoints--fixedpoint"></a><span data-ttu-id="aea40-108">Фикседпоинтс: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span><span class="sxs-lookup"><span data-stu-id="aea40-108">fixedPoints : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span></span>

<span data-ttu-id="aea40-109">Массив чисел с фиксированной запятой, которые будут проверяться на совместимость (с помощью утверждений).</span><span class="sxs-lookup"><span data-stu-id="aea40-109">Array of quantum fixed-point numbers that will be checked for compatibility (using assertions).</span></span>



## <a name="output--unit"></a><span data-ttu-id="aea40-110">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aea40-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

