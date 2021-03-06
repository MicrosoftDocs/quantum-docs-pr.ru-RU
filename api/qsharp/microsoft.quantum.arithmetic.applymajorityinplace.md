---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Операция Апплимажоритинплаце
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: 10b512392b2098663c09b2e07a09c4025da90706
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843727"
---
# <a name="applymajorityinplace-operation"></a>Операция Апплимажоритинплаце

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет кубитную операцию "большинство" на месте к регистру Кубитс.

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Эта операция выполняет вычисление функции большинства на месте 3 Кубитс.

Если мы обкубити выходные данные как $z $ и input Кубитс как $x $ и $y $, операция выполняет следующее преобразование: $ \кет{ксиз} \ригхтарров \кет{КС \оплус z} \кет{и \оплус z} \Кет{\операторнаме{МАЖ} (x, y, z)} $.

## <a name="input"></a>Входные данные

### <a name="output--qubit"></a>выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Первая входная кубит. Обратите внимание, что выходные данные вычисляются на месте и хранятся в этом кубит.


### <a name="input--qubit"></a>входные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Второй и третий входные Кубитс.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

