---
uid: Microsoft.Quantum.Canon.ApplyDiagonalUnitary
title: Операция Апплидиагоналунитари
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits.
ms.openlocfilehash: 8f17c3cb222bef00ead5e7fea5d29d296b9a428a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218858"
---
# <a name="applydiagonalunitary-operation"></a>Операция Апплидиагоналунитари

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет массив сложных фаз к числовым состояниям регистра Кубитс.

```qsharp
operation ApplyDiagonalUnitary (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Эта операция реализует диагональное единое, которое применяет сложный этап $e ^ {i \ theta_j} $ в $n $-кубит номер состояния $ \кет{ж} $.
В частности, эта операция может быть представлена единой

$ $ \бегин{алигн} U = \сум ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \кет{ж}\бра{ж}.
\енд{алигн} $ $

## <a name="input"></a>Входные данные

### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив до $2 ^ n $ коэффициенты $ \ theta_j $. Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.


### <a name="qubits--littleendian"></a>Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

`coefficients` будет дополнен элементами $ \ theta_j = $0,0, если указано меньше $2 ^ n $.

## <a name="references"></a>Ссылки

- Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Аппроксимателяпплидиагоналунитари](xref:Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary)