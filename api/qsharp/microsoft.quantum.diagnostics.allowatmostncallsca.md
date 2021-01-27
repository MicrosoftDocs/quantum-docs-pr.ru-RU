---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Операция Алловатмостнкаллска
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: bb6ba2615b571b0d9d056b93f8e36d2dec0c4a21
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853538"
---
# <a name="allowatmostncallsca-operation"></a>Операция Алловатмостнкаллска

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Между вызовом этой операции и ее прилегающим объектом утверждается, что данная операция вызывается не чаще определенного числа раз.

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="ntimes--int"></a>Нтимес: [int](xref:microsoft.quantum.lang-ref.int)

Максимальное число вызовов, которое `op` может быть вызвано.


### <a name="op--tinput--toutput--is-adj--ctl"></a>Op: "Тинпут =>" Таутпут — "года + CTL"

Операция, вызовы которой должны быть ограничены.


### <a name="message--string"></a>сообщение: [строка](xref:microsoft.quantum.lang-ref.string)

Сообщение, отображаемое при сбое.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="tinput"></a>' Тинпут


### <a name="toutput"></a>' Таутпут



## <a name="example"></a>Пример

Следующий фрагмент кода завершится ошибкой при выполнении на компьютерах, поддерживающих эту диагностику:

```qsharp
using (register = Qubit[4]) {
    within {
        AllowAtMostNCallsCA(3, H, "Too many calls to H.");
    } apply {
        // Fails since this calls H four times, rather than the
        // allowed maximum of three.
        ApplyToEach(H, register);
    }
}
```

## <a name="remarks"></a>Remarks

Эта операция может быть заменена на неработающие целевые объекты, которые не поддерживают эту операцию.