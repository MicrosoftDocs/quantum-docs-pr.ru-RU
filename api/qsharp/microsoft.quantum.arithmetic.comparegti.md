---
uid: Microsoft.Quantum.Arithmetic.CompareGTI
title: Операция Компарегти
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTI
qsharp.summary: 'Wrapper for integer comparison: `result = x > y`.'
ms.openlocfilehash: e9c245fb7c0cf3a6b1b98eb01cd582c325917602
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843300"
---
# <a name="comparegti-operation"></a>Операция Компарегти

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Оболочка для сравнения целых чисел: `result = x > y` .

```qsharp
operation CompareGTI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="xs--littleendian"></a>xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Первое $n $-разрядное число


### <a name="ys--littleendian"></a>ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Второе $n $-разрядное число


### <a name="result--qubit"></a>результат: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Будет отражено, если $x > y $



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

