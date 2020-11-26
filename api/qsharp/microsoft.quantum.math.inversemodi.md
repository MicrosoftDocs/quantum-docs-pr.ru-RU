---
uid: Microsoft.Quantum.Math.InverseModI
title: Функция Инверсемоди
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 217ce4cd113ecbc6a06ed83c6c1dcb7baa46387d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195381"
---
# <a name="inversemodi-function"></a><span data-ttu-id="2dd7e-102">Функция Инверсемоди</span><span class="sxs-lookup"><span data-stu-id="2dd7e-102">InverseModI function</span></span>

<span data-ttu-id="2dd7e-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2dd7e-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2dd7e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2dd7e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2dd7e-105">Возвращает $b $ например, $a \кдот b = 1 (\операторнаме{мод} \тексттт{модулус}) $.</span><span class="sxs-lookup"><span data-stu-id="2dd7e-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModI (a : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="2dd7e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2dd7e-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="2dd7e-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2dd7e-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2dd7e-108">Обратный номер</span><span class="sxs-lookup"><span data-stu-id="2dd7e-108">The number being inverted</span></span>


### <a name="modulus--int"></a><span data-ttu-id="2dd7e-109">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2dd7e-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2dd7e-110">Модуль в соответствии с обратными числами</span><span class="sxs-lookup"><span data-stu-id="2dd7e-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--int"></a><span data-ttu-id="2dd7e-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2dd7e-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2dd7e-112">Целое $b $ например, $a \кдот b = 1 (\операторнаме{мод} \тексттт{модулус}) $.</span><span class="sxs-lookup"><span data-stu-id="2dd7e-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>