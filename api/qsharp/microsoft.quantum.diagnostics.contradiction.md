---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Функция противоречит
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: a5f3f26c5ada2eea9206699a2cc77575a9b5eebd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712864"
---
# <a name="contradiction-function"></a>Функция противоречит

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Объявляет, что классическое условие имеет значение false.

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a>Входные данные

### <a name="actual--bool"></a>фактический: [bool](xref:microsoft.quantum.lang-ref.bool)

Условие, которое необходимо объявить.


### <a name="message--string"></a>сообщение: [строка](xref:microsoft.quantum.lang-ref.string)

Строка сообщения об ошибке для печати в случае, если классическое условие имеет значение true.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Diagnostics. факт](xref:Microsoft.Quantum.Diagnostics.Fact)