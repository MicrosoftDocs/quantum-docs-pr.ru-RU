---
uid: Microsoft.Quantum.Canon.Angle
title: Angle, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: da3ecdaf1b2c88180bd2a660fac0b6e87b2cafa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729761"
---
# <a name="angle-function"></a><span data-ttu-id="40b30-102">Angle, функция</span><span class="sxs-lookup"><span data-stu-id="40b30-102">Angle function</span></span>

<span data-ttu-id="40b30-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="40b30-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="40b30-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="40b30-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="40b30-105">Возвращает значение 1, если `index` имеет нечетное число 1 и-1, если `index` имеет четное число 1.</span><span class="sxs-lookup"><span data-stu-id="40b30-105">Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.</span></span>

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a><span data-ttu-id="40b30-106">Описание</span><span class="sxs-lookup"><span data-stu-id="40b30-106">Description</span></span>

<span data-ttu-id="40b30-107">Значение соответствует знаку коэффициента Rademacher-Walsh спектра из n-переменных и функции для заданного присваивания, которое определяет угол поворота.</span><span class="sxs-lookup"><span data-stu-id="40b30-107">Value corresponds to the sign of the coefficient of the Rademacher-Walsh spectrum of the n-variable AND function for a given assignment that decides the angle of the rotation.</span></span>

## <a name="input"></a><span data-ttu-id="40b30-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="40b30-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="40b30-109">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="40b30-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="40b30-110">Присваивание входных данных в виде целого числа (от 0 до 2 ^ n-1)</span><span class="sxs-lookup"><span data-stu-id="40b30-110">Input assignment as integer (from 0 to 2^n - 1)</span></span>



## <a name="output--int"></a><span data-ttu-id="40b30-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="40b30-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

