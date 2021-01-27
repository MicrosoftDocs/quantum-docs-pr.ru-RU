---
uid: Microsoft.Quantum.Canon.MultiplexZ
title: Операция Мултиплексз
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits.
ms.openlocfilehash: dccfe86104263e23794bce33279e8748f11f5a54
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852428"
---
# <a name="multiplexz-operation"></a>Операция Мултиплексз

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет поворот Паули Z к массиву Кубитс.

```qsharp
operation MultiplexZ (coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Это применяет единую операцию умножения, которая выполняет повороты по угловому оператору $ \ theta_j $ о однокубит Паули operator $Z $ при управлении $n $-кубит номер State $ \кет{ж} $.
В частности, эта операция может быть представлена единой

$ $ \бегин{алигн} U = \сум ^ {2 ^ n-1} _ {j = 0} \кет{ж}\бра{ж} \отимес e ^ {i Z \ theta_j}.
\енд{алигн} $ $

## <a name="input"></a>Входные данные

### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив до $2 ^ n $ коэффициенты $ \ theta_j $. Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.


### <a name="control--littleendian"></a>элемент управления: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Один кубит регистр, повернутый $e ^ {i P \ theta_j} $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

`coefficients` будет дополнен элементами $ \ theta_j = $0,0, если указано меньше $2 ^ n $.

## <a name="references"></a>Ссылки

- Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Аппроксимателимултиплексз](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexZ)