---
uid: Microsoft.Quantum.Math.InverseModL
title: Функция Инверсемодл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModL
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 0d768114c84025a067e0b60762e6834fbd36deb4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228191"
---
# <a name="inversemodl-function"></a><span data-ttu-id="324e0-102">Функция Инверсемодл</span><span class="sxs-lookup"><span data-stu-id="324e0-102">InverseModL function</span></span>

<span data-ttu-id="324e0-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="324e0-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="324e0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="324e0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="324e0-105">Возвращает $b $ например, $a \кдот b = 1 (\операторнаме{мод} \тексттт{модулус}) $.</span><span class="sxs-lookup"><span data-stu-id="324e0-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModL (a : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="324e0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="324e0-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="324e0-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="324e0-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="324e0-108">Обратный номер</span><span class="sxs-lookup"><span data-stu-id="324e0-108">The number being inverted</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="324e0-109">модуль: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="324e0-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="324e0-110">Модуль в соответствии с обратными числами</span><span class="sxs-lookup"><span data-stu-id="324e0-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--bigint"></a><span data-ttu-id="324e0-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="324e0-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="324e0-112">Целое $b $ например, $a \кдот b = 1 (\операторнаме{мод} \тексттт{модулус}) $.</span><span class="sxs-lookup"><span data-stu-id="324e0-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>