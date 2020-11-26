---
uid: Microsoft.Quantum.Math.ModL
title: Функция Модл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModL
qsharp.summary: Returns the modulus of a number with respect to another number.
ms.openlocfilehash: 0b1ac69cc1474e9cfa6a3489b2b2fdf497e812e0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227800"
---
# <a name="modl-function"></a><span data-ttu-id="99fb7-102">Функция Модл</span><span class="sxs-lookup"><span data-stu-id="99fb7-102">ModL function</span></span>

<span data-ttu-id="99fb7-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="99fb7-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="99fb7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="99fb7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="99fb7-105">Возвращает модуль числа по отношению к другому числу.</span><span class="sxs-lookup"><span data-stu-id="99fb7-105">Returns the modulus of a number with respect to another number.</span></span>

```qsharp
function ModL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="99fb7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="99fb7-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="99fb7-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="99fb7-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="99fb7-108">Входной $a $, модуль которого должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="99fb7-108">The input $a$ whose modulus is to be returned.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="99fb7-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="99fb7-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="99fb7-110">Число по отношению к возвращаемому модулю $a $.</span><span class="sxs-lookup"><span data-stu-id="99fb7-110">The number with respect to which the modulus of $a$ is to be returned.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="99fb7-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="99fb7-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="99fb7-112">Модуль $a \бмод b $.</span><span class="sxs-lookup"><span data-stu-id="99fb7-112">The modulus $a \bmod b$.</span></span>