---
uid: Microsoft.Quantum.Canon.ApplyWithA
title: Операция Аппливиса
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: b8847d4b3ddb88031ef360f183b86f6483706cc6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207876"
---
# <a name="applywitha-operation"></a>Операция Аппливиса

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При выполнении двух операций применяется одна, как сопряженная с другой.

```qsharp
operation ApplyWithA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj), target : 'T) : Unit is Adj
```


## <a name="description"></a>Описание

При выполнении двух операций, которые соответственно описаны в единых операторах $U $ и $V $, применяет их в последовательности $U ^ {\дагжер} V U $. Это значит, что эта операция реализует оператор, заданный $V $ сопряженный с $U $.

## <a name="input"></a>Входные данные

### <a name="outeroperation--t--unit--is-adj"></a>Аутероператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода

Операция $U $, которую следует использовать для сопряженного $V $. Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.


### <a name="inneroperation--t--unit--is-adj"></a>Иннероператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода

Операция $V $, для которой выполняется сопряжение.


### <a name="target--t"></a>Целевой объект: 'T

Входные данные, которые должны быть предоставлены внешним и внутренним операциям.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Целевой объект, на котором работают все внутренние и внешние операции.

## <a name="remarks"></a>Комментарии

Во внешней операции всегда предполагается, что это аджоинтабле, но не обязательно быть управляемым, чтобы Объединенная операция была управляемой.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Аппливис](xref:Microsoft.Quantum.Canon.ApplyWith)
- [Microsoft. тактов. Canon. Аппливиск](xref:Microsoft.Quantum.Canon.ApplyWithC)
- [Microsoft. тактов. Canon. Аппливиска](xref:Microsoft.Quantum.Canon.ApplyWithCA)