---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: Функция Форматтедфаилуре
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 6b1202c8897d67e3089a88a0855c8008b3a8c2ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828282"
---
# <a name="formattedfailure-function"></a>Функция Форматтедфаилуре

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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