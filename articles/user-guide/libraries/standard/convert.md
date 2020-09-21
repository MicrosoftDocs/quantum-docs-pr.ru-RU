---
title: Преобразования типов в Q# стандартных библиотеках
description: Сведения об общих и определяемых пользователем функциях преобразования типов в Q# стандартных библиотеках.
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: aa8a1ad624067906998d2735c7a95174a163ce97
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835610"
---
# <a name="type-conversions"></a>Преобразования типов #

Q# — **строго типизированный** язык.
В частности, не Q# выполняет неявное приведение между разными типами. Например, не `1 + 2.0` является допустимым Q# выражением.
Вместо этого Q# предоставляет разнообразные функции преобразования типов для построения новых значений заданного типа.

Например, <xref:microsoft.quantum.core.length> имеет тип выходных данных `Int` , поэтому перед его выводом в `Double` качестве части выражения с плавающей запятой необходимо сначала преобразовать его выходные данные в.
Это можно сделать с помощью <xref:microsoft.quantum.convert.intasdouble> функции:

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<xref:microsoft.quantum.convert>Пространство имен предоставляет общие функции преобразования типов для работы с базовыми встроенными типами, такими как `Int` ,, `Double` `BigInt` , `Result` и `Bool` .

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<xref:microsoft.quantum.convert>Пространство имен также предоставляет еще несколько Exotic преобразований, например `FunctionAsOperation` , которые преобразуют функции `'T -> 'U` в новые операции `'T => 'U` .

Наконец, Q# Стандартная библиотека предоставляет ряд определяемых пользователем типов, таких как <xref:microsoft.quantum.math.complex> и <xref:microsoft.quantum.arithmetic.littleendian> .
Наряду с этими типами Стандартная библиотека предоставляет <xref:microsoft.quantum.arithmetic.bigendianaslittleendian> следующие функции:

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
