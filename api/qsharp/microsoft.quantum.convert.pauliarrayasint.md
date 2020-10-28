---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: Функция Паулиаррайасинт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: f8ec468dd0f0cfd0d868dfc79ff715b3b4fc2f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713368"
---
# <a name="pauliarrayasint-function"></a>Функция Паулиаррайасинт

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакеты [](https://nuget.org/packages/)


Кодирует оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули в целое число.

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a>Входные данные

### <a name="paulis--pauli"></a>Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Массив из не более 31 одного кубит операторов Паули.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Целое число, однозначно идентифицирующее `paulis` , как описано ниже.

## <a name="remarks"></a>Remarks

Каждый оператор Паули может быть закодирован с использованием двух битов: $ $ \бегин{алигн} \болдоне \мапсто 00, \куад X \мапсто 01, \куад Y \мапсто 11, \куад Z \мапсто 10.
\енд{алигн} $ $

При наличии массива операторов Паули `[P0, ..., Pn]` Эта функция возвращает целое число с расширением binary, сформированное путем сцепления сопоставлений каждого оператора Паули в порядке с обратным порядком байтов `bits(Pn) ... bits(P0)` .