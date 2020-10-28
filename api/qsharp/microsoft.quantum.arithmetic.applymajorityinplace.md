---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Операция Апплимажоритинплаце
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: 3664ffe96cd1db8cf5e8898387fe7f2d45b4ea98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731833"
---
# <a name="applymajorityinplace-operation"></a>Операция Апплимажоритинплаце

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Применяет кубитную операцию "большинство" на месте к регистру Кубитс.

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit
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

