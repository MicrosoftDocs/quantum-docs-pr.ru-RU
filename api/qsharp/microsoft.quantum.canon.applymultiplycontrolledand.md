---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledAnd
title: Операция Апплимултипликонтролледанд
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.
ms.openlocfilehash: ac3972287d55ed2df85e1d88510918cc5202c711
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844841"
---
# <a name="applymultiplycontrolledand-operation"></a><span data-ttu-id="fd28b-102">Операция Апплимултипликонтролледанд</span><span class="sxs-lookup"><span data-stu-id="fd28b-102">ApplyMultiplyControlledAnd operation</span></span>

<span data-ttu-id="fd28b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fd28b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fd28b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fd28b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fd28b-105">Реализует многоуправляемый шлюз Тоффоли, предполагая, что целевой кубит инициализирован 0.</span><span class="sxs-lookup"><span data-stu-id="fd28b-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="fd28b-106">При выполнении примыкающей операции предполагается, что целевой кубит будет сброшен в 0.</span><span class="sxs-lookup"><span data-stu-id="fd28b-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>

```qsharp
operation ApplyMultiplyControlledAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="fd28b-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fd28b-107">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="fd28b-108">элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fd28b-108">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fd28b-109">Управление Кубитс</span><span class="sxs-lookup"><span data-stu-id="fd28b-109">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="fd28b-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fd28b-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fd28b-111">Целевой кубит</span><span class="sxs-lookup"><span data-stu-id="fd28b-111">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="fd28b-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fd28b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

