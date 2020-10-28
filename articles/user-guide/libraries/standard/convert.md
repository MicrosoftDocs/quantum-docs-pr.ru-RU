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
ms.openlocfilehash: 9ec3a2ecd2aa59a10a7033e7b3067eb147ce4035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691101"
---
# <a name="type-conversions"></a>Преобразования типов #

Q# — **строго типизированный** язык.
В частности, не Q# выполняет неявное приведение между разными типами. Например, не `1 + 2.0` является допустимым Q# выражением.
Вместо этого Q# предоставляет разнообразные функции преобразования типов для построения новых значений заданного типа.

Например, <xref:Microsoft.Quantum.Core.Length> имеет тип выходных данных `Int` , поэтому перед его выводом в `Double` качестве части выражения с плавающей запятой необходимо сначала преобразовать его выходные данные в.
Это можно сделать с помощью <xref:Microsoft.Quantum.Convert.IntAsDouble> функции:

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<xref:Microsoft.Quantum.Convert>Пространство имен предоставляет общие функции преобразования типов для работы с базовыми встроенными типами, такими как `Int` ,, `Double` `BigInt` , `Result` и `Bool` .

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<xref:Microsoft.Quantum.Convert>Пространство имен также предоставляет еще несколько Exotic преобразований, например `FunctionAsOperation` , которые преобразуют функции `'T -> 'U` в новые операции `'T => 'U` .

Наконец, Q# Стандартная библиотека предоставляет ряд определяемых пользователем типов, таких как <xref:Microsoft.Quantum.Math.Complex> и <xref:Microsoft.Quantum.Arithmetic.LittleEndian> .
Наряду с этими типами Стандартная библиотека предоставляет <xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian> следующие функции:

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
