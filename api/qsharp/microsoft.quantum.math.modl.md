---
uid: Microsoft.Quantum.Math.ModL
title: Функция Модл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModL
qsharp.summary: Returns the modulus of a number with respect to another number.
ms.openlocfilehash: f044ae16d93d31d0f28f5fcf076cff2bfef62eb8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846834"
---
# <a name="modl-function"></a><span data-ttu-id="2c5dc-102">Функция Модл</span><span class="sxs-lookup"><span data-stu-id="2c5dc-102">ModL function</span></span>

<span data-ttu-id="2c5dc-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2c5dc-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2c5dc-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2c5dc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2c5dc-105">Возвращает модуль числа по отношению к другому числу.</span><span class="sxs-lookup"><span data-stu-id="2c5dc-105">Returns the modulus of a number with respect to another number.</span></span>

```qsharp
function ModL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="2c5dc-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2c5dc-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="2c5dc-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2c5dc-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2c5dc-108">Входной $a $, модуль которого должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="2c5dc-108">The input $a$ whose modulus is to be returned.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="2c5dc-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2c5dc-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2c5dc-110">Число по отношению к возвращаемому модулю $a $.</span><span class="sxs-lookup"><span data-stu-id="2c5dc-110">The number with respect to which the modulus of $a$ is to be returned.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="2c5dc-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2c5dc-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2c5dc-112">Модуль $a \бмод b $.</span><span class="sxs-lookup"><span data-stu-id="2c5dc-112">The modulus $a \bmod b$.</span></span>