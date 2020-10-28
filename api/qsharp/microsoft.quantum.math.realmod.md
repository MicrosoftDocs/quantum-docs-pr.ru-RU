---
uid: Microsoft.Quantum.Math.RealMod
title: Функция Реалмод
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 6ec799885bd2f0d35314ed727356499efbe9fcf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731040"
---
# <a name="realmod-function"></a>Функция Реалмод

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакеты [](https://nuget.org/packages/)


Выполняет вычисление модуля между двумя вещественными числами.

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a>Входные данные

### <a name="value--double"></a>значение: [Double](xref:microsoft.quantum.lang-ref.double)

Вещественное число $x $ для получения модуля.


### <a name="modulo--double"></a>остаток от деления: [Double](xref:microsoft.quantum.lang-ref.double)

Вещественное число, взятое из модуля $x $ по отношению к.


### <a name="minvalue--double"></a>minValue: [Double](xref:microsoft.quantum.lang-ref.double)

Наименьшее значение, возвращаемое этой функцией.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Remarks

Эта функция вычислит реальный модуль, заключив реальную строку вокруг единицы круга, а затем находим угол на единицу круга, соответствующую входным данным.
`minValue`Затем входные данные фактически указывают, куда вырезать единицу круга.