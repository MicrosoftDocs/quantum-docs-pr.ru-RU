---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareSparseMultiConfigurationalState
title: Операция Препареспарсемултиконфигуратионалстате
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareSparseMultiConfigurationalState
qsharp.summary: Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.
ms.openlocfilehash: 49b93d0f2447e9eee503bb6ee26aef46c4f5e3f2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98836062"
---
# <a name="preparesparsemulticonfigurationalstate-operation"></a><span data-ttu-id="584a6-102">Операция Препареспарсемултиконфигуратионалстате</span><span class="sxs-lookup"><span data-stu-id="584a6-102">PrepareSparseMultiConfigurationalState operation</span></span>

<span data-ttu-id="584a6-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="584a6-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="584a6-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="584a6-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="584a6-105">Разреженное состояние с несколькими конфигурациями — подготовка пробного состояния путем добавления ексЦитатионс в начальное состояние пробной версии.</span><span class="sxs-lookup"><span data-stu-id="584a6-105">Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.</span></span>

```qsharp
operation PrepareSparseMultiConfigurationalState (initialStatePreparation : (Qubit[] => Unit), excitations : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="584a6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="584a6-106">Input</span></span>

### <a name="initialstatepreparation--qubit--unit"></a><span data-ttu-id="584a6-107">Инитиалстатепрепаратион: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="584a6-107">initialStatePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="584a6-108">Единое для подготовки начального пробного состояния.</span><span class="sxs-lookup"><span data-stu-id="584a6-108">Unitary to prepare initial trial state.</span></span>


### <a name="excitations--jordanwignerinputstate"></a><span data-ttu-id="584a6-109">ексЦитатионс: [жорданвигнеринпутстате](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span><span class="sxs-lookup"><span data-stu-id="584a6-109">excitations : [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span></span>

<span data-ttu-id="584a6-110">ЕксЦитатионс начального пробного состояния, представленного амплитудой ексЦитатион и кубит индексов, с которыми работает ексЦитатион.</span><span class="sxs-lookup"><span data-stu-id="584a6-110">Excitations of initial trial state represented by the amplitude of the excitation and the qubit indices the excitation acts on.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="584a6-111">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="584a6-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="584a6-112">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="584a6-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="584a6-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="584a6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

