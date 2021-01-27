---
uid: Microsoft.Quantum.Math.InverseModI
title: Функция Инверсемоди
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 474146e644bcd042e85b917bc43135a674bedce1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846893"
---
# <a name="inversemodi-function"></a><span data-ttu-id="6a727-102">Функция Инверсемоди</span><span class="sxs-lookup"><span data-stu-id="6a727-102">InverseModI function</span></span>

<span data-ttu-id="6a727-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="6a727-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="6a727-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6a727-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6a727-105">Возвращает $b $ например, $a \кдот b = 1 (\операторнаме{мод} \тексттт{модулус}) $.</span><span class="sxs-lookup"><span data-stu-id="6a727-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModI (a : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="6a727-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6a727-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="6a727-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6a727-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6a727-108">Обратный номер</span><span class="sxs-lookup"><span data-stu-id="6a727-108">The number being inverted</span></span>


### <a name="modulus--int"></a><span data-ttu-id="6a727-109">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6a727-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6a727-110">Модуль в соответствии с обратными числами</span><span class="sxs-lookup"><span data-stu-id="6a727-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--int"></a><span data-ttu-id="6a727-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6a727-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6a727-112">Целое $b $ например, $a \кдот b = 1 (\операторнаме{мод} \тексттт{модулус}) $.</span><span class="sxs-lookup"><span data-stu-id="6a727-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>