---
title: Преобразования типов в Q# стандартных библиотеках
description: Сведения об общих и определяемых пользователем функциях преобразования типов в Q# стандартных библиотеках.
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: 67f47339363a52097f342c8ae4e43a8a93d606a8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858023"
---
# <a name="type-conversions"></a><span data-ttu-id="420a3-103">Преобразования типов</span><span class="sxs-lookup"><span data-stu-id="420a3-103">Type Conversions</span></span> #

<span data-ttu-id="420a3-104">Q# — **строго типизированный** язык.</span><span class="sxs-lookup"><span data-stu-id="420a3-104">Q# is a **strongly-typed** language.</span></span>
<span data-ttu-id="420a3-105">В частности, не Q# выполняет неявное приведение между разными типами.</span><span class="sxs-lookup"><span data-stu-id="420a3-105">In particular, Q# does not implicitly cast between distinct types.</span></span> <span data-ttu-id="420a3-106">Например, не `1 + 2.0` является допустимым Q# выражением.</span><span class="sxs-lookup"><span data-stu-id="420a3-106">For instance, `1 + 2.0` is not a valid Q# expression.</span></span>
<span data-ttu-id="420a3-107">Вместо этого Q# предоставляет разнообразные функции преобразования типов для построения новых значений заданного типа.</span><span class="sxs-lookup"><span data-stu-id="420a3-107">Rather, Q# provides a variety of type conversion functions for constructing new values of a given type.</span></span>

<span data-ttu-id="420a3-108">Например, <xref:Microsoft.Quantum.Core.Length> имеет тип выходных данных `Int` , поэтому перед его выводом в `Double` качестве части выражения с плавающей запятой необходимо сначала преобразовать его выходные данные в.</span><span class="sxs-lookup"><span data-stu-id="420a3-108">For example, <xref:Microsoft.Quantum.Core.Length> has an output type of `Int`, so its output must first be converted to a `Double` before it can be used as a part of a floating-point expression.</span></span>
<span data-ttu-id="420a3-109">Это можно сделать с помощью <xref:Microsoft.Quantum.Convert.IntAsDouble> функции:</span><span class="sxs-lookup"><span data-stu-id="420a3-109">This can be done using the <xref:Microsoft.Quantum.Convert.IntAsDouble> function:</span></span>

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<span data-ttu-id="420a3-110"><xref:Microsoft.Quantum.Convert>Пространство имен предоставляет общие функции преобразования типов для работы с базовыми встроенными типами, такими как `Int` ,, `Double` `BigInt` , `Result` и `Bool` .</span><span class="sxs-lookup"><span data-stu-id="420a3-110">The <xref:Microsoft.Quantum.Convert> namespace provides common type conversion functions for working with the basic built-in types, such as `Int`, `Double`, `BigInt`, `Result`, and `Bool`:</span></span>

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<span data-ttu-id="420a3-111"><xref:Microsoft.Quantum.Convert>Пространство имен также предоставляет еще несколько Exotic преобразований, например `FunctionAsOperation` , которые преобразуют функции `'T -> 'U` в новые операции `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="420a3-111">The <xref:Microsoft.Quantum.Convert> namespace also provides some more exotic conversions, such as `FunctionAsOperation`, which converts functions `'T -> 'U` into new operations `'T => 'U`.</span></span>

<span data-ttu-id="420a3-112">Наконец, Q# Стандартная библиотека предоставляет ряд определяемых пользователем типов, таких как <xref:Microsoft.Quantum.Math.Complex> и <xref:Microsoft.Quantum.Arithmetic.LittleEndian> .</span><span class="sxs-lookup"><span data-stu-id="420a3-112">Finally, the Q# standard library provides a number of user-defined types such as <xref:Microsoft.Quantum.Math.Complex> and <xref:Microsoft.Quantum.Arithmetic.LittleEndian>.</span></span>
<span data-ttu-id="420a3-113">Наряду с этими типами Стандартная библиотека предоставляет <xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian> следующие функции:</span><span class="sxs-lookup"><span data-stu-id="420a3-113">Along with these types, the standard library provides functions such as <xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian>:</span></span>

```qsharp
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
