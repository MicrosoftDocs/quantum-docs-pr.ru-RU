---
uid: Microsoft.Quantum.Canon.ApplyWithC
title: Операция Аппливиск
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithC
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: 8de1ddf0bf176853b33926be7647bc5d1d35095d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716896"
---
# <a name="applywithc-operation"></a>Операция Аппливиск

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


При выполнении двух операций применяется одна, как сопряженная с другой.

```qsharp
operation ApplyWithC<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Ctl), target : 'T) : Unit
```


## <a name="description"></a>Описание

При выполнении двух операций, которые соответственно описаны в единых операторах $U $ и $V $, применяет их в последовательности $U ^ {\дагжер} V U $. Это значит, что эта операция реализует оператор, заданный $V $ сопряженный с $U $.

## <a name="input"></a>Входные данные

### <a name="outeroperation--t--unit-adj"></a>Аутероператион: 'T [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода

Операция $U $, которую следует использовать для сопряженного $V $. Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.


### <a name="inneroperation--t--unit-ctl"></a>Иннероператион: 'T = список CTL для [единицы](xref:microsoft.quantum.lang-ref.unit)>

Операция $V $, для которой выполняется сопряжение.


### <a name="target--t"></a>Целевой объект: 'T

Входные данные, которые должны быть предоставлены внешним и внутренним операциям.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Целевой объект, на котором работают все внутренние и внешние операции.

## <a name="remarks"></a>Remarks

Во внешней операции всегда предполагается, что это аджоинтабле, но не обязательно быть управляемым, чтобы Объединенная операция была управляемой.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Аппливис](xref:Microsoft.Quantum.Canon.ApplyWith)
- [Microsoft. тактов. Canon. Аппливиса](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [Microsoft. тактов. Canon. Аппливиска](xref:Microsoft.Quantum.Canon.ApplyWithCA)