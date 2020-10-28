---
uid: Microsoft.Quantum.Math.ModL
title: Функция Модл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModL
qsharp.summary: Returns the modulus of a number with respect to another number.
ms.openlocfilehash: 15b11a59d189aa881da9fb514cf0fe3bc9f20201
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732705"
---
# <a name="modl-function"></a><span data-ttu-id="bf2aa-102">Функция Модл</span><span class="sxs-lookup"><span data-stu-id="bf2aa-102">ModL function</span></span>

<span data-ttu-id="bf2aa-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="bf2aa-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="bf2aa-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bf2aa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bf2aa-105">Возвращает модуль числа по отношению к другому числу.</span><span class="sxs-lookup"><span data-stu-id="bf2aa-105">Returns the modulus of a number with respect to another number.</span></span>

```qsharp
function ModL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="bf2aa-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bf2aa-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="bf2aa-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="bf2aa-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="bf2aa-108">Входной $a $, модуль которого должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="bf2aa-108">The input $a$ whose modulus is to be returned.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="bf2aa-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="bf2aa-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="bf2aa-110">Число по отношению к возвращаемому модулю $a $.</span><span class="sxs-lookup"><span data-stu-id="bf2aa-110">The number with respect to which the modulus of $a$ is to be returned.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="bf2aa-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="bf2aa-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="bf2aa-112">Модуль $a \бмод b $.</span><span class="sxs-lookup"><span data-stu-id="bf2aa-112">The modulus $a \bmod b$.</span></span>