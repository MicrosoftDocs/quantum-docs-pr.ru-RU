---
uid: Microsoft.Quantum.Math.InverseModL
title: Функция Инверсемодл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModL
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: e7cb9e98cb0635c50162611f6a52c56027d4a5eb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733008"
---
# <a name="inversemodl-function"></a><span data-ttu-id="829b6-102">Функция Инверсемодл</span><span class="sxs-lookup"><span data-stu-id="829b6-102">InverseModL function</span></span>

<span data-ttu-id="829b6-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="829b6-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="829b6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="829b6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="829b6-105">Возвращает $b $ например, $a \кдот b = 1 (\операторнаме{мод} \тексттт{модулус}) $.</span><span class="sxs-lookup"><span data-stu-id="829b6-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModL (a : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="829b6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="829b6-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="829b6-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="829b6-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="829b6-108">Обратный номер</span><span class="sxs-lookup"><span data-stu-id="829b6-108">The number being inverted</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="829b6-109">модуль: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="829b6-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="829b6-110">Модуль в соответствии с обратными числами</span><span class="sxs-lookup"><span data-stu-id="829b6-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--bigint"></a><span data-ttu-id="829b6-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="829b6-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="829b6-112">Целое $b $ например, $a \кдот b = 1 (\операторнаме{мод} \тексттт{модулус}) $.</span><span class="sxs-lookup"><span data-stu-id="829b6-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>