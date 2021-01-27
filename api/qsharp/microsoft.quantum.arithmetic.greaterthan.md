---
uid: Microsoft.Quantum.Arithmetic.GreaterThan
title: Операция GreaterThan
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: GreaterThan
qsharp.summary: Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.
ms.openlocfilehash: 553efb0fc83f24235cb4a77933bd1d547bbd1fed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846629"
---
# <a name="greaterthan-operation"></a>Операция GreaterThan

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет сравнение типа "больше" между двумя целыми числами, закодированными в регистры кубит, зеркальное отображение целевого кубит на основе результата сравнения.

```qsharp
operation GreaterThan (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Выполняет строго больше сравнений двух целых чисел $x $ и $y $, закодированных в кубит регистры XS и ИС. Если $x > y $, результат будет отражен кубит, в противном случае результат кубит будет оставаться в прежнем состоянии.

## <a name="input"></a>Входные данные

### <a name="xs--littleendian"></a>xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Литтлиндиан кубит закодировать первое целое число $x $.


### <a name="ys--littleendian"></a>ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Литтлиндиан кубит зарегистрировать второе целое число $y $.


### <a name="result--qubit"></a>результат: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Один кубит, который будет отражен, если $x > y $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Использует прием, который $x-y = (x "+ y)" $, где "обозначает дополнение одного.

## <a name="references"></a>Ссылки

- Андрей A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон: "Новая тактовая цепь Ripple — комплексное сложение", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1

- Томас Хаенер, Мартен Роеттелер, Криста M. Своре: "факторинг с использованием 2N + 2 Кубитс с модульным умножением на основе Тоффоли", 2016 https://arxiv.org/abs/1611.07995