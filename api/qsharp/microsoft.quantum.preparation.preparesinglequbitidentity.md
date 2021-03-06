---
uid: Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity
title: Операция Препаресинглекубитидентити
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareSingleQubitIdentity
qsharp.summary: >-
  Prepares a qubit in the maximally mixed state.

  It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.
ms.openlocfilehash: c6c9b5724354d6ee034dd8b6733901ebdd8072d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856872"
---
# <a name="preparesinglequbitidentity-operation"></a>Операция Препаресинглекубитидентити

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Подготавливает кубит в максимально смешанном состоянии.

Он подготавливает заданный кубит в состоянии $ \болдоне/$2, применяя канал деполаризинг $ $ \бегин{алигн} \Омега (\рхо) \масрел{: =} \фрак {1} {4} \ sum_ {\му \ин \{ 0, 1, 2, 3 \} } \сигма \_ {\му} \rho \sigma \_ {\mu} ^ {\dagger}, \end{align} $ $, где $ \sigma \_ i $ — $i $ TH Pauli, где $ \rho $ — оператор плотности, представляющий смешанное состояние.

```qsharp
operation PrepareSingleQubitIdentity (qubit : Qubit) : Unit
```


## <a name="input"></a>Входные данные

### <a name="qubit--qubit"></a>Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Объект кубит, состояние которого необходимо деполяровать, как описано выше.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Смешанное состояние $ \болдоне/$2, описывающее результат применения этой операции к состоянию, неявно описывает значение ожидания для случайных вариантов, сделанных в этой операции.
Таким образом, для любого отдельного приложения эта операция сопоставляет чистые состояния с чистыми состояниями, но действует, как описано в разделе ожидание.
В частности, эта операция может использоваться в процессе томографи для измерения *небазовых* компонентов канала.