---
uid: Microsoft.Quantum.Canon.MultiplexOperationsWithAuxRegister
title: Операция Мултиплексоператионсвисауксрегистер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsWithAuxRegister
qsharp.summary: Implementation step of MultiplexOperations.
ms.openlocfilehash: 91db22d6261709c1c3506c80ff600c904748575a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852458"
---
# <a name="multiplexoperationswithauxregister-operation"></a><span data-ttu-id="11adb-102">Операция Мултиплексоператионсвисауксрегистер</span><span class="sxs-lookup"><span data-stu-id="11adb-102">MultiplexOperationsWithAuxRegister operation</span></span>

<span data-ttu-id="11adb-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="11adb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="11adb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="11adb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="11adb-105">Шаг реализации Мултиплексоператионс.</span><span class="sxs-lookup"><span data-stu-id="11adb-105">Implementation step of MultiplexOperations.</span></span>

```qsharp
operation MultiplexOperationsWithAuxRegister<'T> (unitaries : ('T => Unit is Adj + Ctl)[], auxillaryRegister : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="11adb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="11adb-106">Input</span></span>

### <a name="unitaries--t--unit--is-adj--ctl"></a><span data-ttu-id="11adb-107">унитариес: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL []"</span><span class="sxs-lookup"><span data-stu-id="11adb-107">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>




### <a name="auxillaryregister--qubit"></a><span data-ttu-id="11adb-108">Ауксилларирегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="11adb-108">auxillaryRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="index--littleendian"></a><span data-ttu-id="11adb-109">Индекс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="11adb-109">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="target--t"></a><span data-ttu-id="11adb-110">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="11adb-110">target : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="11adb-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="11adb-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="11adb-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="11adb-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="11adb-113">Е</span><span class="sxs-lookup"><span data-stu-id="11adb-113">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="11adb-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="11adb-114">See Also</span></span>

- [<span data-ttu-id="11adb-115">Microsoft. тактов. Canon. Мултиплексоператионс</span><span class="sxs-lookup"><span data-stu-id="11adb-115">Microsoft.Quantum.Canon.MultiplexOperations</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperations)