---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledLowDepthAnd
title: Операция Апплимултипликонтролледловдепсанд
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledLowDepthAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.  Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.
ms.openlocfilehash: 1aeab429bd6304c621e0d5225b43a76eab607c84
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209202"
---
# <a name="applymultiplycontrolledlowdepthand-operation"></a><span data-ttu-id="6e9b1-102">Операция Апплимултипликонтролледловдепсанд</span><span class="sxs-lookup"><span data-stu-id="6e9b1-102">ApplyMultiplyControlledLowDepthAnd operation</span></span>

<span data-ttu-id="6e9b1-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6e9b1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6e9b1-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6e9b1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6e9b1-105">Реализует многоуправляемый шлюз Тоффоли, предполагая, что целевой кубит инициализирован 0.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="6e9b1-106">При выполнении примыкающей операции предполагается, что целевой кубит будет сброшен в 0.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>  <span data-ttu-id="6e9b1-107">Требуется РЗ глубина 1, а число вспомогательных Кубитс — экспоненциальное число Кубитс.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-107">Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.</span></span>

```qsharp
operation ApplyMultiplyControlledLowDepthAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="6e9b1-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6e9b1-108">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="6e9b1-109">элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6e9b1-109">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6e9b1-110">Управление Кубитс</span><span class="sxs-lookup"><span data-stu-id="6e9b1-110">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="6e9b1-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6e9b1-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6e9b1-112">Целевой кубит</span><span class="sxs-lookup"><span data-stu-id="6e9b1-112">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="6e9b1-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6e9b1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

