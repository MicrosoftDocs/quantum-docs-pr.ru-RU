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
# <a name="type-conversions"></a><span data-ttu-id="31510-103">Преобразования типов</span><span class="sxs-lookup"><span data-stu-id="31510-103">Type Conversions</span></span> #

<span data-ttu-id="31510-104">Q # — **строго типизированный** язык.</span><span class="sxs-lookup"><span data-stu-id="31510-104">Q# is a **strongly-typed** language.</span></span>
<span data-ttu-id="31510-105">В частности, Q # не приводит к неявному приведению между разными типами.</span><span class="sxs-lookup"><span data-stu-id="31510-105">In particular, Q# does not implicitly cast between distinct types.</span></span> <span data-ttu-id="31510-106">Например, `1 + 2.0` не является допустимым выражением Q #.</span><span class="sxs-lookup"><span data-stu-id="31510-106">For instance, `1 + 2.0` is not a valid Q# expression.</span></span>
<span data-ttu-id="31510-107">Вместо этого Q # предоставляет разнообразные функции преобразования типов для построения новых значений заданного типа.</span><span class="sxs-lookup"><span data-stu-id="31510-107">Rather, Q# provides a variety of type conversion functions for constructing new values of a given type.</span></span>

<span data-ttu-id="31510-108">Например, <xref:microsoft.quantum.core.length> имеет тип выходных данных `Int`, поэтому его выходные данные необходимо сначала преобразовать в `Double`, прежде чем его можно будет использовать в качестве части выражения с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="31510-108">For example, <xref:microsoft.quantum.core.length> has an output type of `Int`, so its output must first be converted to a `Double` before it can be used as a part of a floating-point expression.</span></span>
<span data-ttu-id="31510-109">Это можно сделать с помощью функции <xref:microsoft.quantum.convert.intasdouble>:</span><span class="sxs-lookup"><span data-stu-id="31510-109">This can be done using the <xref:microsoft.quantum.convert.intasdouble> function:</span></span>

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<span data-ttu-id="31510-110">Пространство имен <xref:microsoft.quantum.convert> предоставляет общие функции преобразования типов для работы с базовыми встроенными типами, такими как `Int`, `Double`, `BigInt`, `Result`и `Bool`.</span><span class="sxs-lookup"><span data-stu-id="31510-110">The <xref:microsoft.quantum.convert> namespace provides common type conversion functions for working with the basic built-in types, such as `Int`, `Double`, `BigInt`, `Result`, and `Bool`:</span></span>

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<span data-ttu-id="31510-111">Пространство имен <xref:microsoft.quantum.convert> также предоставляет еще несколько преобразований Exotic, таких как `FunctionAsOperation`, которые преобразуют функции `'T -> 'U` в новые операции `'T => 'U`.</span><span class="sxs-lookup"><span data-stu-id="31510-111">The <xref:microsoft.quantum.convert> namespace also provides some more exotic conversions, such as `FunctionAsOperation`, which converts functions `'T -> 'U` into new operations `'T => 'U`.</span></span>

<span data-ttu-id="31510-112">Наконец, стандартная библиотека Q # предоставляет ряд определяемых пользователем типов, таких как <xref:microsoft.quantum.math.complex> и <xref:microsoft.quantum.arithmetic.littleendian>.</span><span class="sxs-lookup"><span data-stu-id="31510-112">Finally, the Q# standard library provides a number of user-defined types such as <xref:microsoft.quantum.math.complex> and <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>
<span data-ttu-id="31510-113">Наряду с этими типами Стандартная библиотека предоставляет такие функции, как <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:</span><span class="sxs-lookup"><span data-stu-id="31510-113">Along with these types, the standard library provides functions such as <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:</span></span>

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
