---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: Операция Аддфксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: 60b7cad3d0bd8800e67830ca921f8e2d705b8f39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843859"
---
# <a name="addfxp-operation"></a>Операция Аддфксп

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Добавляет два числа с фиксированной запятой, хранящихся в тактовых регистрах.

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

При наличии двух регистров с фиксированной запятой соответственно в состояниях $ \кет{f_1} $ и $ \кет{f_2} $ выполняет операцию $ \кет{f_1} \кет{f_2} \мапсто \кет{f_1} \кет{f_1 + f_2} $.

## <a name="input"></a>Входные данные

### <a name="fp1--fixedpoint"></a>FP1: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Первое число с фиксированной запятой


### <a name="fp2--fixedpoint"></a>Fp2: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Второе число с фиксированной запятой будет обновлено для включения суммы двух входных значений.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Для текущей реализации требуется, чтобы два числа с фиксированной запятой имели одинаковую позицию точки с наименьшего значащим битом, т. е. $n _i $ и $p _i $ должны быть равны.