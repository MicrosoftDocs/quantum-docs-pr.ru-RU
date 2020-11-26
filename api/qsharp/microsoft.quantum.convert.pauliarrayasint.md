---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: Функция Паулиаррайасинт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: 6077110cc07c8626b22eb404c1de096ed43efcc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224247"
---
# <a name="pauliarrayasint-function"></a>Функция Паулиаррайасинт

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Кодирует оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули в целое число.

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a>Входные данные

### <a name="paulis--pauli"></a>Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Массив из не более 31 одного кубит операторов Паули.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Целое число, однозначно идентифицирующее `paulis` , как описано ниже.

## <a name="remarks"></a>Комментарии

Каждый оператор Паули может быть закодирован с использованием двух битов: $ $ \бегин{алигн} \болдоне \мапсто 00, \куад X \мапсто 01, \куад Y \мапсто 11, \куад Z \мапсто 10.
\енд{алигн} $ $

При наличии массива операторов Паули `[P0, ..., Pn]` Эта функция возвращает целое число с расширением binary, сформированное путем сцепления сопоставлений каждого оператора Паули в порядке с обратным порядком байтов `bits(Pn) ... bits(P0)` .