---
uid: Microsoft.Quantum.Math.InverseModI
title: Функция Инверсемоди
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 6efc9da5f5ebb64065a90e749daa629dc2dce9cf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733009"
---
# <a name="inversemodi-function"></a><span data-ttu-id="249e0-102">Функция Инверсемоди</span><span class="sxs-lookup"><span data-stu-id="249e0-102">InverseModI function</span></span>

<span data-ttu-id="249e0-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="249e0-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="249e0-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="249e0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="249e0-105">Возвращает $b $ например, $a \кдот b = 1 (\операторнаме{мод} \тексттт{модулус}) $.</span><span class="sxs-lookup"><span data-stu-id="249e0-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModI (a : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="249e0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="249e0-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="249e0-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="249e0-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="249e0-108">Обратный номер</span><span class="sxs-lookup"><span data-stu-id="249e0-108">The number being inverted</span></span>


### <a name="modulus--int"></a><span data-ttu-id="249e0-109">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="249e0-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="249e0-110">Модуль в соответствии с обратными числами</span><span class="sxs-lookup"><span data-stu-id="249e0-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--int"></a><span data-ttu-id="249e0-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="249e0-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="249e0-112">Целое $b $ например, $a \кдот b = 1 (\операторнаме{мод} \тексттт{модулус}) $.</span><span class="sxs-lookup"><span data-stu-id="249e0-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>