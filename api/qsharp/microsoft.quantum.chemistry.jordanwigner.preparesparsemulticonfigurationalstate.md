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
# <a name="preparesparsemulticonfigurationalstate-operation"></a>Операция Препареспарсемултиконфигуратионалстате

Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Разреженное состояние с несколькими конфигурациями — подготовка пробного состояния путем добавления ексЦитатионс в начальное состояние пробной версии.

```qsharp
operation PrepareSparseMultiConfigurationalState (initialStatePreparation : (Qubit[] => Unit), excitations : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], qubits : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="initialstatepreparation--qubit--unit"></a>Инитиалстатепрепаратион: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Единое для подготовки начального пробного состояния.


### <a name="excitations--jordanwignerinputstate"></a>ексЦитатионс: [жорданвигнеринпутстате](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]

ЕксЦитатионс начального пробного состояния, представленного амплитудой ексЦитатион и кубит индексов, с которыми работает ексЦитатион.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубитс Хамилтониан.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

