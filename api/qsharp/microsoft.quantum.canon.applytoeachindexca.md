---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: Операция Апплитоеачиндекска
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: abb616498a8ff9c3348df81cf0ca1a1669561eec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208947"
---
# <a name="applytoeachindexca-operation"></a><span data-ttu-id="cebda-102">Операция Апплитоеачиндекска</span><span class="sxs-lookup"><span data-stu-id="cebda-102">ApplyToEachIndexCA operation</span></span>

<span data-ttu-id="cebda-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cebda-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cebda-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cebda-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cebda-105">Применяет одну операцию кубит к каждому индексированному элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="cebda-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="cebda-106">Модификатор `CA` указывает, что операция с одним кубитом является аджоинтабле и управляемой.</span><span class="sxs-lookup"><span data-stu-id="cebda-106">The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.</span></span>

```qsharp
operation ApplyToEachIndexCA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="cebda-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cebda-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj--ctl"></a><span data-ttu-id="cebda-108">Синглилементоператион: ([int](xref:microsoft.quantum.lang-ref.int), 't) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="cebda-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="cebda-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="cebda-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="cebda-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="cebda-110">register : 'T[]</span></span>

<span data-ttu-id="cebda-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="cebda-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cebda-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cebda-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cebda-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="cebda-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cebda-114">Е</span><span class="sxs-lookup"><span data-stu-id="cebda-114">'T</span></span>

<span data-ttu-id="cebda-115">Целевой объект, на котором действует каждая из операций.</span><span class="sxs-lookup"><span data-stu-id="cebda-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="cebda-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="cebda-116">See Also</span></span>

- [<span data-ttu-id="cebda-117">Microsoft. тактов. Canon. Апплитоеачиндекс</span><span class="sxs-lookup"><span data-stu-id="cebda-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)