---
uid: Microsoft.Quantum.Canon.ApplyWith
title: Операция Аппливис
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWith
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: 7127df047a260b18d75efb092e8e090e2d0b207a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850411"
---
# <a name="applywith-operation"></a>Операция Аппливис

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При выполнении двух операций применяется одна, как сопряженная с другой.

```qsharp
operation ApplyWith<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit), target : 'T) : Unit
```


## <a name="description"></a>Описание

При выполнении двух операций, которые соответственно описаны в единых операторах $U $ и $V $, применяет их в последовательности $U ^ {\дагжер} V U $. Это значит, что эта операция реализует оператор, заданный $V $ сопряженный с $U $.

## <a name="input"></a>Входные данные

### <a name="outeroperation--t--unit--is-adj"></a>Аутероператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода

Операция $U $, которую следует использовать для сопряженного $V $. Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.


### <a name="inneroperation--t--unit"></a>Иннероператион: 'T = [единица](xref:microsoft.quantum.lang-ref.unit)> 

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

- [Microsoft. тактов. Canon. Аппливиса](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [Microsoft. тактов. Canon. Аппливиск](xref:Microsoft.Quantum.Canon.ApplyWithC)
- [Microsoft. тактов. Canon. Аппливиска](xref:Microsoft.Quantum.Canon.ApplyWithCA)