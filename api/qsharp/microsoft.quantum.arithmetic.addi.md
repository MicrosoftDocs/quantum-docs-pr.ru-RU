---
uid: Microsoft.Quantum.Arithmetic.AddI
title: Операция Адди
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: a17403652cc2b2712defe52112a3ac599330da9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843848"
---
# <a name="addi-operation"></a>Операция Адди

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Автоматически выбирает между добавлением и без, в зависимости от размера регистра `ys` .

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="xs--littleendian"></a>xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-bit слагаемое.


### <a name="ys--littleendian"></a>ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Слагаемое по крайней мере $n $ Кубитс. Будет содержать результат.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

