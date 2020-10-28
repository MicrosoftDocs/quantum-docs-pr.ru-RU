---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledAnd
title: Операция Апплимултипликонтролледанд
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.
ms.openlocfilehash: feca28d394e4af31eb4ffe737111d00ede45e27e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717959"
---
# <a name="applymultiplycontrolledand-operation"></a><span data-ttu-id="33529-102">Операция Апплимултипликонтролледанд</span><span class="sxs-lookup"><span data-stu-id="33529-102">ApplyMultiplyControlledAnd operation</span></span>

<span data-ttu-id="33529-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="33529-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="33529-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="33529-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="33529-105">Реализует многоуправляемый шлюз Тоффоли, предполагая, что целевой кубит инициализирован 0.</span><span class="sxs-lookup"><span data-stu-id="33529-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="33529-106">При выполнении примыкающей операции предполагается, что целевой кубит будет сброшен в 0.</span><span class="sxs-lookup"><span data-stu-id="33529-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>

```qsharp
operation ApplyMultiplyControlledAnd (controls : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="33529-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="33529-107">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="33529-108">элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="33529-108">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="33529-109">Управление Кубитс</span><span class="sxs-lookup"><span data-stu-id="33529-109">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="33529-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="33529-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="33529-111">Целевой кубит</span><span class="sxs-lookup"><span data-stu-id="33529-111">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="33529-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="33529-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

