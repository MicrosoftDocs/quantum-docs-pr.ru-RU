---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE._prepareTrialStateWrapper
title: _prepareTrialStateWrapper операция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: _prepareTrialStateWrapper
qsharp.summary: Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint. EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.
ms.openlocfilehash: f0deba39d834731fd9057a1d40d0c78b2b7e6bb8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850222"
---
# <a name="_preparetrialstatewrapper-operation"></a>_prepareTrialStateWrapper операция

Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Частная оболочка вокруг Препаретриалстате, чтобы обеспечить совместимость с Естиматефрекуенциа путем определения примыкающего.
Естиматефрекуенциа имеет встроенную функцию эмуляции, предназначенную для Куантумсимулатор, которая ускоряет выполнение.

```qsharp
operation _prepareTrialStateWrapper (inputState : (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), qubits : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="inputstate--intjordanwignerinputstate"></a>Инпутстате: ([int](xref:microsoft.quantum.lang-ref.int),[жорданвигнеринпутстате](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])

Для запуска Препаретриалстате требуются входные данные Jordan-Wigner.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубит регистр.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

