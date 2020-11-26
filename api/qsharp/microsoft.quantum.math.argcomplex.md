---
uid: Microsoft.Quantum.Math.ArgComplex
title: Функция Аргкомплекс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 259296f397207cde4a7d6dfe6cfb1a18e8055216
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211106"
---
# <a name="argcomplex-function"></a>Функция Аргкомплекс

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает фазу комплексного числа типа `Complex` .

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>Входные данные

### <a name="input--complex"></a>входные данные: [сложные](xref:Microsoft.Quantum.Math.Complex)

Комплексное число $c = x + i y $.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

Этап $ \Текст{АРГ} [c] = \Текст{арктан} (y, x) \ин (-\пи, \пи] $).