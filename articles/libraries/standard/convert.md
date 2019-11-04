---
title: 'Q # Стандартные библиотеки — преобразования типов | Документация Майкрософт'
description: 'Q # Стандартные библиотеки — преобразования типов'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: 4716f0d9562229f08ef6f0f5f80961f793de4c5c
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2019
ms.locfileid: "73184480"
---
# <a name="type-conversions"></a>Преобразования типов #

Q # — **строго типизированный** язык.
В частности, Q # не приводит к неявному приведению между разными типами. Например, `1 + 2.0` не является допустимым выражением Q #.
Вместо этого Q # предоставляет разнообразные функции преобразования типов для построения новых значений заданного типа.

Например, <xref:microsoft.quantum.core.length> имеет тип выходных данных `Int`, поэтому его выходные данные необходимо сначала преобразовать в `Double`, прежде чем его можно будет использовать в качестве части выражения с плавающей запятой.
Это можно сделать с помощью функции <xref:microsoft.quantum.convert.intasdouble>:

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

Пространство имен <xref:microsoft.quantum.convert> предоставляет общие функции преобразования типов для работы с базовыми встроенными типами, такими как `Int`, `Double`, `BigInt`, `Result`и `Bool`.

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

Пространство имен <xref:microsoft.quantum.convert> также предоставляет еще несколько преобразований Exotic, таких как `FunctionAsOperation`, которые преобразуют функции `'T -> 'U` в новые операции `'T => 'U`.

Наконец, стандартная библиотека Q # предоставляет ряд определяемых пользователем типов, таких как <xref:microsoft.quantum.math.complex> и <xref:microsoft.quantum.arithmetic.littleendian>.
Наряду с этими типами Стандартная библиотека предоставляет такие функции, как <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
