---
uid: Microsoft.Quantum.Diagnostics.Fact
title: Функция фактов
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Fact
qsharp.summary: Declares that a classical condition is true.
ms.openlocfilehash: 6a08703f68f9f38f2224fe4c6a4d255b00756908
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712682"
---
# <a name="fact-function"></a>Функция фактов

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Объявляет, что классическое условие имеет значение true.

```qsharp
function Fact (actual : Bool, message : String) : Unit
```


## <a name="input"></a>Входные данные

### <a name="actual--bool"></a>фактический: [bool](xref:microsoft.quantum.lang-ref.bool)

Условие, которое необходимо объявить.


### <a name="message--string"></a>сообщение: [строка](xref:microsoft.quantum.lang-ref.string)

Строка сообщения об ошибке для печати в случае, если классический параметр имеет значение false.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Diagnostics. противоречит](xref:Microsoft.Quantum.Diagnostics.Contradiction)