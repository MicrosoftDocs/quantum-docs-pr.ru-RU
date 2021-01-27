---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Функция Иснотзеро
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 9384e5dafd4b5b7d44cb348c9537ebc2c621466d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839597"
---
# <a name="isnotzero-function"></a><span data-ttu-id="90588-102">Функция Иснотзеро</span><span class="sxs-lookup"><span data-stu-id="90588-102">IsNotZero function</span></span>

<span data-ttu-id="90588-103">Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="90588-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="90588-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="90588-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="90588-105">Проверяет `Double` , не равен ли число приблизительно нулю.</span><span class="sxs-lookup"><span data-stu-id="90588-105">Checks whether a `Double` number is not approximately zero.</span></span>

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="90588-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="90588-106">Input</span></span>

### <a name="number--double"></a><span data-ttu-id="90588-107">число: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="90588-107">number : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="90588-108">Число для проверки</span><span class="sxs-lookup"><span data-stu-id="90588-108">Number to be checked</span></span>



## <a name="output--bool"></a><span data-ttu-id="90588-109">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="90588-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="90588-110">Возвращает значение true `number` , если имеет абсолютное значение больше `1e-15` .</span><span class="sxs-lookup"><span data-stu-id="90588-110">Returns true if `number` has an absolute value greater than `1e-15`.</span></span>