---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: Функция Аллекуалитифактб
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 79dcf65956ba9436fb6fdd452f22f35d4852d6f8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213707"
---
# <a name="allequalityfactb-function"></a><span data-ttu-id="5a507-102">Функция Аллекуалитифактб</span><span class="sxs-lookup"><span data-stu-id="5a507-102">AllEqualityFactB function</span></span>

<span data-ttu-id="5a507-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="5a507-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="5a507-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5a507-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5a507-105">Утверждает, что два массива логических значений равны.</span><span class="sxs-lookup"><span data-stu-id="5a507-105">Asserts that two arrays of boolean values are equal.</span></span>

```qsharp
function AllEqualityFactB (actual : Bool[], expected : Bool[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="5a507-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5a507-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="5a507-107">фактический: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="5a507-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="5a507-108">Массив, создаваемый тестовым случаем.</span><span class="sxs-lookup"><span data-stu-id="5a507-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="5a507-109">ожидалось: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="5a507-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="5a507-110">Массив, который ожидается из тестового случая, представляющего интерес.</span><span class="sxs-lookup"><span data-stu-id="5a507-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="5a507-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="5a507-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="5a507-112">Выводимое сообщение, если массивы не равны.</span><span class="sxs-lookup"><span data-stu-id="5a507-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5a507-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5a507-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

