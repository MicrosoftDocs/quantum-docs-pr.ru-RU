---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Операция Апплитоеачиндекс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 8b34dc24580a3df7ae2c13ef87a6fa10c7afd3f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844594"
---
# <a name="applytoeachindex-operation"></a><span data-ttu-id="2c181-102">Операция Апплитоеачиндекс</span><span class="sxs-lookup"><span data-stu-id="2c181-102">ApplyToEachIndex operation</span></span>

<span data-ttu-id="2c181-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2c181-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2c181-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2c181-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2c181-105">Применяет одну операцию кубит к каждому индексированному элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="2c181-105">Applies a single-qubit operation to each indexed element in a register.</span></span>

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="2c181-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2c181-106">Input</span></span>

### <a name="singleelementoperation--intt--unit"></a><span data-ttu-id="2c181-107">Синглилементоператион: ([int](xref:microsoft.quantum.lang-ref.int), t) = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="2c181-107">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="2c181-108">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="2c181-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="2c181-109">Register: не []</span><span class="sxs-lookup"><span data-stu-id="2c181-109">register : 'T[]</span></span>

<span data-ttu-id="2c181-110">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="2c181-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2c181-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2c181-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2c181-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2c181-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2c181-113">Е</span><span class="sxs-lookup"><span data-stu-id="2c181-113">'T</span></span>

<span data-ttu-id="2c181-114">Целевой объект, на котором действует каждая из операций.</span><span class="sxs-lookup"><span data-stu-id="2c181-114">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c181-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="2c181-115">See Also</span></span>

- [<span data-ttu-id="2c181-116">Microsoft. тактов. Canon. Апплитоеач</span><span class="sxs-lookup"><span data-stu-id="2c181-116">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [<span data-ttu-id="2c181-117">Microsoft. тактов. Canon. Апплитоеачиндекса</span><span class="sxs-lookup"><span data-stu-id="2c181-117">Microsoft.Quantum.Canon.ApplyToEachIndexA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [<span data-ttu-id="2c181-118">Microsoft. тактов. Canon. Апплитоеачиндекск</span><span class="sxs-lookup"><span data-stu-id="2c181-118">Microsoft.Quantum.Canon.ApplyToEachIndexC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [<span data-ttu-id="2c181-119">Microsoft. тактов. Canon. Апплитоеачиндекска</span><span class="sxs-lookup"><span data-stu-id="2c181-119">Microsoft.Quantum.Canon.ApplyToEachIndexCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)