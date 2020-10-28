---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Операция Рефлектабаутинтежер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: e034f0a24d5c2f0465ebd1914b28cb8c695d978c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730577"
---
# <a name="reflectaboutinteger-operation"></a>Операция Рефлектабаутинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Отражает тактовый регистр относительно заданного классического целого числа.

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Описание

С учетом регистра такта изначально находится в состоянии $ \ sum_i \ alpha_i \кет{и} $, где каждый $ \кет{и} $ является исходным состоянием, представляющим целое число $i $, отражает состояние регистра относительно базового состояния для заданного целого числа $ \кет{ж} $, $ $ \ sum_i (-1) ^ {\ delta_ {ИЖ}} \ alpha_i \кет{и} $ $

## <a name="input"></a>Входные данные

### <a name="index--int"></a>Индекс: [int](xref:microsoft.quantum.lang-ref.int)

Классическое целое число, которое индексирует состояние основания, относительно которого будет отражаться.


### <a name="reg--littleendian"></a>reg: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Эта операция реализуется на месте без явного выделения дополнительных вспомогательных Кубитс.