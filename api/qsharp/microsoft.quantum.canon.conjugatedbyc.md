---
uid: Microsoft.Quantum.Canon.ConjugatedByC
title: Функция Конжугатедбик
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByC
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: 1aa471a0f9039151d130bd52a026f4c1a0765e32
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216682"
---
# <a name="conjugatedbyc-function"></a>Функция Конжугатедбик

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии внешних и внутренних операций возвращает новую операцию, которая сопряжена с внутренней операцией внешней операцией.

```qsharp
function ConjugatedByC<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Ctl)) : ('T => Unit is Ctl)
```


## <a name="input"></a>Входные данные

### <a name="outeroperation--t--unit--is-adj"></a>Аутероператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода

Операция $U $, которую следует использовать для сопряженного $V $. Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.


### <a name="inneroperation--t--unit--is-ctl"></a>Иннероператион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL

Операция $V $, для которой выполняется сопряжение.



## <a name="output--t--unit--is-ctl"></a>Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL

Новая операция, действие которой представляется единой $U ^ {\дагжер} V U $.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип целевого объекта, в котором работают все внутренние и внешние операции.

## <a name="remarks"></a>Комментарии

Во внешней операции всегда предполагается, что это аджоинтабле, но не обязательно быть управляемым, чтобы Объединенная операция была управляемой.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Конжугатедби](xref:Microsoft.Quantum.Canon.ConjugatedBy)
- [Microsoft. тактов. Canon. Конжугатедбя](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [Microsoft. тактов. Canon. Конжугатедбика](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [Microsoft. тактов. Canon. Аппливис](xref:Microsoft.Quantum.Canon.ApplyWith)