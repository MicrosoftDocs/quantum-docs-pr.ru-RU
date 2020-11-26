---
uid: Microsoft.Quantum.Chemistry.JordanWigner.SelectZ
title: Операция Селектз
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: SelectZ
qsharp.summary: A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$. That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$
ms.openlocfilehash: 08abe3f465432bf98f35090c59fb4d952c3b4882
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224723"
---
# <a name="selectz-operation"></a>Операция Селектз

Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Единая $U $, которая применяет шлюз Паули $Z $ к Кубитс $p $ с состоянием индекса $ \кет{п} $. Т. е. $ $ \бегин{алигн} У\кет {p} \ Сисакет {\ PSI} = \Кет{п}з \_ п\кет {\ PSI} \енд{алигн} $ $

```qsharp
operation SelectZ (indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="indexregister--littleendian"></a>Индексрегистер: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Состояние $ \кет{п} $ этого регистра определяет кубит, к которому применяется $Z $.


### <a name="targetregister--qubit"></a>Таржетрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация Кубитс, к которой применяются операторы Паули.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

