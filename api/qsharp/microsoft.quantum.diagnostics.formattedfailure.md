---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: Функция Форматтедфаилуре
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 0d7fb01ddf23cd6d79f722c8f6b691afa74a8885
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712681"
---
# <a name="formattedfailure-function"></a>Функция Форматтедфаилуре

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Внутренняя функция, используемая для сбоя с осмысленными сообщениями об ошибках.

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a>Входные данные

### <a name="actual--t"></a>фактический: нет




### <a name="expected--t"></a>ожидалось: 'T




### <a name="message--string"></a>сообщение: [строка](xref:microsoft.quantum.lang-ref.string)





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Remarks

Эта функция предназначена для имитации средой выполнения моделирования, поэтому она позволяет пересылать необработанные соответствия.