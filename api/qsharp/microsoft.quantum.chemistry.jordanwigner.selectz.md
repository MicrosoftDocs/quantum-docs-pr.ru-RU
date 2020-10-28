---
uid: Microsoft.Quantum.Chemistry.JordanWigner.SelectZ
title: Операция Селектз
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: SelectZ
qsharp.summary: A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$. That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$
ms.openlocfilehash: 171bbe28ce8f10ca4b213a94b23f8c049546e3bf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713788"
---
# <a name="selectz-operation"></a>Операция Селектз

Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Пакеты [](https://nuget.org/packages/)


Единая $U $, которая применяет шлюз Паули $Z $ к Кубитс $p $ с состоянием индекса $ \кет{п} $. Т. е. $ $ \бегин{алигн} У\кет {p} \ Сисакет {\ PSI} = \Кет{п}з \_ п\кет {\ PSI} \енд{алигн} $ $

```qsharp
operation SelectZ (indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="indexregister--littleendian"></a>Индексрегистер: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Состояние $ \кет{п} $ этого регистра определяет кубит, к которому применяется $Z $.


### <a name="targetregister--qubit"></a>Таржетрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация Кубитс, к которой применяются операторы Паули.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

