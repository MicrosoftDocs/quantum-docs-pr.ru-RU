---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryStateD
title: Операция Препареарбитраристатед
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryStateD
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: 61f6614821951435828cd28edeb1447cb33f3648
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842373"
---
# <a name="preparearbitrarystated-operation"></a>Операция Препареарбитраристатед

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Учитывая набор коэффициентов и регистр такта с прямым порядком байтов, подготавливает к этому регистру состояние, описываемое заданным коэффициентом.

```qsharp
operation PrepareArbitraryStateD (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Эта операция подготавливает произвольное состояние такта $ \кет{\пси} $ с сложными коэффициентами $r _j e ^ {i t_j} $ из $n $-кубит вычислительное состояние $ \ket{0 \кдотс 0} $.
В частности, действие этой операции может быть смоделировано единым преобразованием $U $, которое работает в состоянии «все-нули», как

$ $ \бегин{алигн} У\кет {0... 0} & = \кет{\пси} \\ \\ & = \фрак{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \кет{ж}} {\скрт{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.
\енд{алигн} $ $

## <a name="input"></a>Входные данные

### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив до $2 ^ n $ Real коэффициентов. Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.


### <a name="qubits--littleendian"></a>Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Кубит регистр номеров кодировки в формате с прямым порядком байтов. Это должно быть инициализировано в состоянии вычислительной базы $ \ket{0...0} $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Отрицательные коэффициенты ввода $r _j < $0 будут рассматриваться как положительные значения $ | r_j | $. `coefficients` будет дополнен элементами $ (r_j, t_j) = (0,0, 0,0) $, если указано меньше $2 ^ n $.

## <a name="references"></a>Ссылки

- Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. подготовка. Аппроксимателипрепареарбитраристате](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)