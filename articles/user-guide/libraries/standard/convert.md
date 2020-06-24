---
title: 'Преобразования типов в стандартных библиотеках Q #'
description: 'Сведения об общих и определяемых пользователем функциях преобразования типов в стандартных библиотеках Q #.'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: e941d7e3d76459546861410e91a03d7315183867
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275740"
---
# <a name="type-conversions"></a>Преобразования типов #

Q # — **строго типизированный** язык.
В частности, Q # не приводит к неявному приведению между разными типами. Например, не `1 + 2.0` является допустимым выражением Q #.
Вместо этого Q # предоставляет разнообразные функции преобразования типов для построения новых значений заданного типа.

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

Наконец, стандартная библиотека Q # предоставляет ряд определяемых пользователем типов, таких как <xref:microsoft.quantum.math.complex> и <xref:microsoft.quantum.arithmetic.littleendian> .
Наряду с этими типами Стандартная библиотека предоставляет <xref:microsoft.quantum.arithmetic.bigendianaslittleendian> следующие функции:

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
