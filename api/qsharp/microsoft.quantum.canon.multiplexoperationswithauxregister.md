---
uid: Microsoft.Quantum.Canon.MultiplexOperationsWithAuxRegister
title: Операция Мултиплексоператионсвисауксрегистер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsWithAuxRegister
qsharp.summary: Implementation step of MultiplexOperations.
ms.openlocfilehash: 530e78ba0c5ce6e0627177527daf2ccc56f537eb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205989"
---
# <a name="multiplexoperationswithauxregister-operation"></a><span data-ttu-id="c42af-102">Операция Мултиплексоператионсвисауксрегистер</span><span class="sxs-lookup"><span data-stu-id="c42af-102">MultiplexOperationsWithAuxRegister operation</span></span>

<span data-ttu-id="c42af-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c42af-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c42af-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c42af-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c42af-105">Шаг реализации Мултиплексоператионс.</span><span class="sxs-lookup"><span data-stu-id="c42af-105">Implementation step of MultiplexOperations.</span></span>

```qsharp
operation MultiplexOperationsWithAuxRegister<'T> (unitaries : ('T => Unit is Adj + Ctl)[], auxillaryRegister : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c42af-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c42af-106">Input</span></span>

### <a name="unitaries--t--unit--is-adj--ctl"></a><span data-ttu-id="c42af-107">унитариес: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL []"</span><span class="sxs-lookup"><span data-stu-id="c42af-107">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>




### <a name="auxillaryregister--qubit"></a><span data-ttu-id="c42af-108">Ауксилларирегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c42af-108">auxillaryRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="index--littleendian"></a><span data-ttu-id="c42af-109">Индекс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c42af-109">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="target--t"></a><span data-ttu-id="c42af-110">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="c42af-110">target : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="c42af-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c42af-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c42af-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c42af-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c42af-113">Е</span><span class="sxs-lookup"><span data-stu-id="c42af-113">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="c42af-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="c42af-114">See Also</span></span>

- [<span data-ttu-id="c42af-115">Microsoft. тактов. Canon. Мултиплексоператионс</span><span class="sxs-lookup"><span data-stu-id="c42af-115">Microsoft.Quantum.Canon.MultiplexOperations</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperations)