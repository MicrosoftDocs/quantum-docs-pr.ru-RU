---
uid: Microsoft.Quantum.Chemistry.JordanWigner.SelectZ
title: Операция Селектз
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: SelectZ
qsharp.summary: A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$. That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$
ms.openlocfilehash: 2b38be5c196d81635daa8b478f6e727fdf378c62
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850239"
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

