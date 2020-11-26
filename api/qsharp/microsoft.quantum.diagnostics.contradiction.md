---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Функция противоречит
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: f9ad9a7d67bda8e50c76f679f535ad55ba07698e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202147"
---
# <a name="contradiction-function"></a>Функция противоречит

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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