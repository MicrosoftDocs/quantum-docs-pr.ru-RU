---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: Операция Скуареси
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7fe4d27b974a06b019a2b15710fbc51b598027b4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221833"
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



## <a name="remarks"></a>Комментарии

Реализация основывается на Интежерскуаре.