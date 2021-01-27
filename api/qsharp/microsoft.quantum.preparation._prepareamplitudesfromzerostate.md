---
uid: Microsoft.Quantum.Preparation._PrepareAmplitudesFromZeroState
title: _PrepareAmplitudesFromZeroState операция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: _PrepareAmplitudesFromZeroState
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register of unentangled qubits, all of which are in zero state, prepares a state on that register described by the given coefficients. Uses state emulation if supported by the target.
ms.openlocfilehash: 94563632d514f66608b14c264a73bdfcc6f50982
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854445"
---
# <a name="_prepareamplitudesfromzerostate-operation"></a>_PrepareAmplitudesFromZeroState операция

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Учитывая набор коэффициентов и регистр такта с прямым порядком байтов для унентанглед Кубитс, все из которых находятся в нулевом состоянии, подготавливает состояние для этой регистрации, описываемой этими коэффициентами. Использует эмуляцию состояния, если поддерживается целевым объектом.

```qsharp
operation _PrepareAmplitudesFromZeroState (coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Входные данные

### <a name="coefficients--complexpolar"></a>коэффициенты: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)[]




### <a name="qubits--littleendian"></a>Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

