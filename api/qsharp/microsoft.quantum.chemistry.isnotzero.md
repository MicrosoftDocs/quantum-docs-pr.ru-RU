---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Функция Иснотзеро
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: f80dbba6a51e62970e87c2782faba558340d2bd8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204068"
---
# <a name="isnotzero-function"></a><span data-ttu-id="c4a82-102">Функция Иснотзеро</span><span class="sxs-lookup"><span data-stu-id="c4a82-102">IsNotZero function</span></span>

<span data-ttu-id="c4a82-103">Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="c4a82-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="c4a82-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="c4a82-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="c4a82-105">Проверяет `Double` , не равен ли число приблизительно нулю.</span><span class="sxs-lookup"><span data-stu-id="c4a82-105">Checks whether a `Double` number is not approximately zero.</span></span>

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="c4a82-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c4a82-106">Input</span></span>

### <a name="number--double"></a><span data-ttu-id="c4a82-107">число: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c4a82-107">number : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c4a82-108">Число для проверки</span><span class="sxs-lookup"><span data-stu-id="c4a82-108">Number to be checked</span></span>



## <a name="output--bool"></a><span data-ttu-id="c4a82-109">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c4a82-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c4a82-110">Возвращает значение true `number` , если имеет абсолютное значение больше `1e-15` .</span><span class="sxs-lookup"><span data-stu-id="c4a82-110">Returns true if `number` has an absolute value greater than `1e-15`.</span></span>