---
uid: Microsoft.Quantum.Canon.RepeatA
title: Операция Repeat
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 9ae3123a64b2a886df3b7575b2840522f9b011ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852222"
---
# <a name="repeata-operation"></a>Операция Repeat

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Повторяет операцию заданное число раз.

```qsharp
operation RepeatA<'TInput> (op : ('TInput => Unit is Adj), nTimes : Int, input : 'TInput) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="op--tinput--unit--is-adj"></a>Op: ' Тинпут =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  в сумме

Операция, которая вызывается повторно.


### <a name="ntimes--int"></a>Нтимес: [int](xref:microsoft.quantum.lang-ref.int)

Число вызовов `op` .


### <a name="input--tinput"></a>входные данные: ' Тинпут

Входные данные, передаваемые в `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="tinput"></a>' Тинпут



## <a name="example"></a>Пример

Следующие эквивалентны:

```qsharp
RepeatA(U, 17, target);
(BoundA(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. Дравмани](xref:Microsoft.Quantum.Arrays.DrawMany)
- [Microsoft. тактов. Canon. REPEAT](xref:Microsoft.Quantum.Canon.Repeat)
- [Microsoft. тактов. Canon. Репеатк](xref:Microsoft.Quantum.Canon.RepeatC)
- [Microsoft. тактов. Canon. Репеатка](xref:Microsoft.Quantum.Canon.RepeatCA)