---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledAnd
title: Операция Апплимултипликонтролледанд
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.
ms.openlocfilehash: 17a757278500833bc5a5d0635af020cfe1fd569f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218399"
---
# <a name="applymultiplycontrolledand-operation"></a><span data-ttu-id="bd1dd-102">Операция Апплимултипликонтролледанд</span><span class="sxs-lookup"><span data-stu-id="bd1dd-102">ApplyMultiplyControlledAnd operation</span></span>

<span data-ttu-id="bd1dd-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bd1dd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bd1dd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bd1dd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bd1dd-105">Реализует многоуправляемый шлюз Тоффоли, предполагая, что целевой кубит инициализирован 0.</span><span class="sxs-lookup"><span data-stu-id="bd1dd-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="bd1dd-106">При выполнении примыкающей операции предполагается, что целевой кубит будет сброшен в 0.</span><span class="sxs-lookup"><span data-stu-id="bd1dd-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>

```qsharp
operation ApplyMultiplyControlledAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="bd1dd-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bd1dd-107">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="bd1dd-108">элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bd1dd-108">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bd1dd-109">Управление Кубитс</span><span class="sxs-lookup"><span data-stu-id="bd1dd-109">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="bd1dd-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bd1dd-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="bd1dd-111">Целевой кубит</span><span class="sxs-lookup"><span data-stu-id="bd1dd-111">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="bd1dd-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bd1dd-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

