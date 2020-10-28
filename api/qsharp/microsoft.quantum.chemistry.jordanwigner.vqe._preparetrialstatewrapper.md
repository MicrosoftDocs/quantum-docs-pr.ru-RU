---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE._prepareTrialStateWrapper
title: _prepareTrialStateWrapper операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: _prepareTrialStateWrapper
qsharp.summary: Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint. EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.
ms.openlocfilehash: bfd7b9ce8e8b2c8f322d676c640f8c2488655516
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713760"
---
# <a name="_preparetrialstatewrapper-operation"></a><span data-ttu-id="e85c1-102">_prepareTrialStateWrapper операция</span><span class="sxs-lookup"><span data-stu-id="e85c1-102">_prepareTrialStateWrapper operation</span></span>

<span data-ttu-id="e85c1-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="e85c1-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="e85c1-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e85c1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e85c1-105">Частная оболочка вокруг Препаретриалстате, чтобы обеспечить совместимость с Естиматефрекуенциа путем определения примыкающего.</span><span class="sxs-lookup"><span data-stu-id="e85c1-105">Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint.</span></span>
<span data-ttu-id="e85c1-106">Естиматефрекуенциа имеет встроенную функцию эмуляции, предназначенную для Куантумсимулатор, которая ускоряет выполнение.</span><span class="sxs-lookup"><span data-stu-id="e85c1-106">EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.</span></span>

```qsharp
operation _prepareTrialStateWrapper (inputState : (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e85c1-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e85c1-107">Input</span></span>

### <a name="inputstate--intjordanwignerinputstate"></a><span data-ttu-id="e85c1-108">Инпутстате: ([int](xref:microsoft.quantum.lang-ref.int),[жорданвигнеринпутстате](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])</span><span class="sxs-lookup"><span data-stu-id="e85c1-108">inputState : ([Int](xref:microsoft.quantum.lang-ref.int),[JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])</span></span>

<span data-ttu-id="e85c1-109">Для запуска Препаретриалстате требуются входные данные Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="e85c1-109">The Jordan-Wigner input required for PrepareTrialState to run.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="e85c1-110">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e85c1-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e85c1-111">Кубит регистр.</span><span class="sxs-lookup"><span data-stu-id="e85c1-111">A qubit register.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e85c1-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e85c1-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

