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
# <a name="type-conversions"></a><span data-ttu-id="96d42-103">Преобразования типов</span><span class="sxs-lookup"><span data-stu-id="96d42-103">Type Conversions</span></span> #

<span data-ttu-id="96d42-104">Q# — **строго типизированный** язык.</span><span class="sxs-lookup"><span data-stu-id="96d42-104">Q# is a **strongly-typed** language.</span></span>
<span data-ttu-id="96d42-105">В частности, не Q# выполняет неявное приведение между разными типами.</span><span class="sxs-lookup"><span data-stu-id="96d42-105">In particular, Q# does not implicitly cast between distinct types.</span></span> <span data-ttu-id="96d42-106">Например, не `1 + 2.0` является допустимым Q# выражением.</span><span class="sxs-lookup"><span data-stu-id="96d42-106">For instance, `1 + 2.0` is not a valid Q# expression.</span></span>
<span data-ttu-id="96d42-107">Вместо этого Q# предоставляет разнообразные функции преобразования типов для построения новых значений заданного типа.</span><span class="sxs-lookup"><span data-stu-id="96d42-107">Rather, Q# provides a variety of type conversion functions for constructing new values of a given type.</span></span>

<span data-ttu-id="96d42-108">Например, <xref:microsoft.quantum.core.length> имеет тип выходных данных `Int` , поэтому перед его выводом в `Double` качестве части выражения с плавающей запятой необходимо сначала преобразовать его выходные данные в.</span><span class="sxs-lookup"><span data-stu-id="96d42-108">For example, <xref:microsoft.quantum.core.length> has an output type of `Int`, so its output must first be converted to a `Double` before it can be used as a part of a floating-point expression.</span></span>
<span data-ttu-id="96d42-109">Это можно сделать с помощью <xref:microsoft.quantum.convert.intasdouble> функции:</span><span class="sxs-lookup"><span data-stu-id="96d42-109">This can be done using the <xref:microsoft.quantum.convert.intasdouble> function:</span></span>

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<span data-ttu-id="96d42-110"><xref:microsoft.quantum.convert>Пространство имен предоставляет общие функции преобразования типов для работы с базовыми встроенными типами, такими как `Int` ,, `Double` `BigInt` , `Result` и `Bool` .</span><span class="sxs-lookup"><span data-stu-id="96d42-110">The <xref:microsoft.quantum.convert> namespace provides common type conversion functions for working with the basic built-in types, such as `Int`, `Double`, `BigInt`, `Result`, and `Bool`:</span></span>

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<span data-ttu-id="96d42-111"><xref:microsoft.quantum.convert>Пространство имен также предоставляет еще несколько Exotic преобразований, например `FunctionAsOperation` , которые преобразуют функции `'T -> 'U` в новые операции `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="96d42-111">The <xref:microsoft.quantum.convert> namespace also provides some more exotic conversions, such as `FunctionAsOperation`, which converts functions `'T -> 'U` into new operations `'T => 'U`.</span></span>

<span data-ttu-id="96d42-112">Наконец, Q# Стандартная библиотека предоставляет ряд определяемых пользователем типов, таких как <xref:microsoft.quantum.math.complex> и <xref:microsoft.quantum.arithmetic.littleendian> .</span><span class="sxs-lookup"><span data-stu-id="96d42-112">Finally, the Q# standard library provides a number of user-defined types such as <xref:microsoft.quantum.math.complex> and <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>
<span data-ttu-id="96d42-113">Наряду с этими типами Стандартная библиотека предоставляет <xref:microsoft.quantum.arithmetic.bigendianaslittleendian> следующие функции:</span><span class="sxs-lookup"><span data-stu-id="96d42-113">Along with these types, the standard library provides functions such as <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:</span></span>

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
