---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareSparseMultiConfigurationalState
title: Операция Препареспарсемултиконфигуратионалстате
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareSparseMultiConfigurationalState
qsharp.summary: Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.
ms.openlocfilehash: 4d39be70c48ed49a1eec410ed6f8e5081dc1e8ca
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224774"
---
# <a name="preparesparsemulticonfigurationalstate-operation"></a><span data-ttu-id="64a78-102">Операция Препареспарсемултиконфигуратионалстате</span><span class="sxs-lookup"><span data-stu-id="64a78-102">PrepareSparseMultiConfigurationalState operation</span></span>

<span data-ttu-id="64a78-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="64a78-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="64a78-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="64a78-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="64a78-105">Разреженное состояние с несколькими конфигурациями — подготовка пробного состояния путем добавления ексЦитатионс в начальное состояние пробной версии.</span><span class="sxs-lookup"><span data-stu-id="64a78-105">Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.</span></span>

```qsharp
operation PrepareSparseMultiConfigurationalState (initialStatePreparation : (Qubit[] => Unit), excitations : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="64a78-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="64a78-106">Input</span></span>

### <a name="initialstatepreparation--qubit--unit"></a><span data-ttu-id="64a78-107">Инитиалстатепрепаратион: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="64a78-107">initialStatePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="64a78-108">Единое для подготовки начального пробного состояния.</span><span class="sxs-lookup"><span data-stu-id="64a78-108">Unitary to prepare initial trial state.</span></span>


### <a name="excitations--jordanwignerinputstate"></a><span data-ttu-id="64a78-109">ексЦитатионс: [жорданвигнеринпутстате](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span><span class="sxs-lookup"><span data-stu-id="64a78-109">excitations : [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span></span>

<span data-ttu-id="64a78-110">ЕксЦитатионс начального пробного состояния, представленного амплитудой ексЦитатион и кубит индексов, с которыми работает ексЦитатион.</span><span class="sxs-lookup"><span data-stu-id="64a78-110">Excitations of initial trial state represented by the amplitude of the excitation and the qubit indices the excitation acts on.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="64a78-111">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="64a78-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="64a78-112">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="64a78-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="64a78-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64a78-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

