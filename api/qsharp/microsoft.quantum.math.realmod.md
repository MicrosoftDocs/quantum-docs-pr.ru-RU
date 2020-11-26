---
uid: Microsoft.Quantum.Math.RealMod
title: Функция Реалмод
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 20916d8462288395384aa875bfae4f042ba6b6ad
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228259"
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



## <a name="remarks"></a>Комментарии

Эта функция вычислит реальный модуль, заключив реальную строку вокруг единицы круга, а затем находим угол на единицу круга, соответствующую входным данным.
`minValue`Затем входные данные фактически указывают, куда вырезать единицу круга.