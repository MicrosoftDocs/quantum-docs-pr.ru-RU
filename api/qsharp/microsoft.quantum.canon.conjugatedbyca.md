---
uid: Microsoft.Quantum.Canon.ConjugatedByCA
title: Функция Конжугатедбика
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByCA
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: 54301f991d3bda14e2d2a0a6837ee89d299f2e04
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840816"
---
# <a name="conjugatedbyca-function"></a>Функция Конжугатедбика

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии внешних и внутренних операций возвращает новую операцию, которая сопряжена с внутренней операцией внешней операцией.

```qsharp
function ConjugatedByCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl)) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="outeroperation--t--unit--is-adj"></a>Аутероператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода

Операция $U $, которую следует использовать для сопряженного $V $. Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.


### <a name="inneroperation--t--unit--is-adj--ctl"></a>Иннероператион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция $V $, для которой выполняется сопряжение.



## <a name="output--t--unit--is-adj--ctl"></a>Выходные данные: 'T => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)  и CTL

Новая операция, действие которой представляется единой $U ^ {\дагжер} V U $.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип целевого объекта, в котором работают все внутренние и внешние операции.

## <a name="remarks"></a>Remarks

Во внешней операции всегда предполагается, что это аджоинтабле, но не обязательно быть управляемым, чтобы Объединенная операция была управляемой.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Конжугатедбя](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [Microsoft. тактов. Canon. Конжугатедбик](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [Microsoft. тактов. Canon. Конжугатедбика](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [Microsoft. тактов. Canon. Аппливис](xref:Microsoft.Quantum.Canon.ApplyWith)