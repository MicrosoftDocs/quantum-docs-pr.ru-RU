---
uid: Microsoft.Quantum.Math.RealMod
title: Функция Реалмод
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 56da313fabb20655ec358120b8d9b435e4971159
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848352"
---
# <a name="realmod-function"></a>Функция Реалмод

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="example"></a>Пример

```qsharp
    // Returns 3 π / 2.
    let y = RealMod(5.5 * PI(), 2.0 * PI(), 0.0);
    // Returns -1.2, since +3.6 and -1.2 are 4.8 apart on the real line,
    // which is a multiple of 2.4.
    let z = RealMod(3.6, 2.4, -1.2);
```

## <a name="remarks"></a>Remarks

Эта функция вычислит реальный модуль, заключив реальную строку вокруг единицы круга, а затем находим угол на единицу круга, соответствующую входным данным.
`minValue`Затем входные данные фактически указывают, куда вырезать единицу круга.