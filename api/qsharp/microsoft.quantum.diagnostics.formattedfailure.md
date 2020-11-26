---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: Функция Форматтедфаилуре
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: da809c04059d4fd0f0ec92412a3094f5b582fd91
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201705"
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



## <a name="remarks"></a>Комментарии

Эта функция предназначена для имитации средой выполнения моделирования, поэтому она позволяет пересылать необработанные соответствия.