---
uid: Microsoft.Quantum.Math.ArgComplex
title: Функция Аргкомплекс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: e8ce73a43940ab0ed66338f962cc6f76fc2b694b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842755"
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