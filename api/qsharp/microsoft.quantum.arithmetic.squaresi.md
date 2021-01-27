---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: Операция Скуареси
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 161b45766c6f4d500d25def24aa509ee7fdc8628
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842929"
---
# <a name="squaresi-operation"></a>Операция Скуареси

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Квадратное целое число со знаком `xs` и сохранение результата в `result` , который должен быть равен нулю изначально.

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="xs--signedlittleendian"></a>xs: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

n-разрядное целое число в квадрат (Сигнедлиттлиндиан)


### <a name="result--signedlittleendian"></a>результат: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

2N-разрядный результат (Сигнедлиттлиндиан) должен находиться в состоянии $ \кет {0} $ изначально.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Реализация основывается на Интежерскуаре.