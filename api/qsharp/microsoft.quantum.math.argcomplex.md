---
uid: Microsoft.Quantum.Math.ArgComplex
title: Функция Аргкомплекс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 629aa32ad80e5aa3d6f5ff75ac65df9b1a96fc15
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732800"
---
# <a name="argcomplex-function"></a>Функция Аргкомплекс

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакеты [](https://nuget.org/packages/)


Возвращает фазу комплексного числа типа `Complex` .

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>Входные данные

### <a name="input--complex"></a>входные данные: [сложные](xref:Microsoft.Quantum.Math.Complex)

Комплексное число $c = x + i y $.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

Этап $ \Текст{АРГ} [c] = \Текст{арктан} (y, x) \ин (-\пи, \пи] $).