---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Операция Рефлектабаутинтежер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: 4d451c4e8e002f86c892b394f58ea2d7e9dd6a48
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842974"
---
# <a name="reflectaboutinteger-operation"></a>Операция Рефлектабаутинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Отражает тактовый регистр относительно заданного классического целого числа.

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
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