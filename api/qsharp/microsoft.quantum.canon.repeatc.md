---
uid: Microsoft.Quantum.Canon.RepeatC
title: Операция Репеатк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: efb820411be63352fc09ada2441a9140dd5575f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840237"
---
# <a name="repeatc-operation"></a>Операция Репеатк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Повторяет операцию заданное число раз.

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit is Ctl
```


## <a name="input"></a>Входные данные

### <a name="op--tinput--unit--is-ctl"></a>Op: "Тинпут = [Unit](xref:microsoft.quantum.lang-ref.unit) > является CTL

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
RepeatC(U, 17, target);
(BoundC(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. Дравмани](xref:Microsoft.Quantum.Arrays.DrawMany)
- [Microsoft. тактов. Canon. REPEAT](xref:Microsoft.Quantum.Canon.Repeat)
- [Microsoft. тактов. Canon. REPEAT](xref:Microsoft.Quantum.Canon.RepeatA)
- [Microsoft. тактов. Canon. Репеатка](xref:Microsoft.Quantum.Canon.RepeatCA)