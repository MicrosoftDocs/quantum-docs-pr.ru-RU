---
uid: Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli
title: Операция Аппроксимателимултиплекспаули
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyMultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 1fc8a8857b6b37d4c3e812a3c4cb2941b9238800
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844575"
---
# <a name="approximatelymultiplexpauli-operation"></a>Операция Аппроксимателимултиплекспаули

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет вращение Паули к массиву Кубитс, округляя небольшие углы вращения в соответствии с заданным отклонением.

```qsharp
operation ApproximatelyMultiplexPauli (tolerance : Double, coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Это применяет единую операцию умножения, которая выполняет повороты по угловому оператору $ \ theta_j $ о однокубит Паули operator $P $ при управлении $n $-кубит номер State $ \кет{ж} $.
В частности, действие этой операции представлено единым

$ $ \бегин{алигн} U = \сум ^ {2 ^ n-1} _ {j = 0} \кет{ж}\бра{ж} \отимес e ^ {i P \ theta_j}.
\енд{алигн}

##

## <a name="input"></a>Входные данные

### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Допуск, ниже которого усекаются небольшие коэффициенты.


### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив до $2 ^ n $ коэффициенты $ \ theta_j $. Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.


### <a name="pauli--pauli"></a>Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Оператор Паули $P $, определяющий ось вращения.


### <a name="control--littleendian"></a>элемент управления: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Один кубит регистр, повернутый $e ^ {i P \ theta_j} $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

`coefficients` будет дополнен элементами $ \ theta_j = $0,0, если указано меньше $2 ^ n $.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Мултиплекспаули](xref:Microsoft.Quantum.Canon.MultiplexPauli)