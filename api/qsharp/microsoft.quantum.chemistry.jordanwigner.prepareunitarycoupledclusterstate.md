---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareUnitaryCoupledClusterState
title: Операция Препареунитарикаупледклустерстате
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareUnitaryCoupledClusterState
qsharp.summary: Unitary coupled-cluster state preparation of trial state
ms.openlocfilehash: 1d5b8963bd50752fef22fea0a3c002e3e2ebc90a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98836036"
---
# <a name="prepareunitarycoupledclusterstate-operation"></a>Операция Препареунитарикаупледклустерстате

Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Единое связывание — подготовка состояния для пробного использования в кластере

```qsharp
operation PrepareUnitaryCoupledClusterState (initialStatePreparation : (Qubit[] => Unit), clusterOperator : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], trotterStepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="initialstatepreparation--qubit--unit"></a>Инитиалстатепрепаратион: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Единое для подготовки начального пробного состояния.


### <a name="clusteroperator--jordanwignerinputstate"></a>Клустероператор: [жорданвигнеринпутстате](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]




### <a name="trotterstepsize--double"></a>Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)




### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубитс Хамилтониан.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

