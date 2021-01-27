---
uid: Microsoft.Quantum.Diagnostics.Fact
title: Функция фактов
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Fact
qsharp.summary: Declares that a classical condition is true.
ms.openlocfilehash: 8e86000f04c01040d420c2f682fc1b4ccf35cf39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853307"
---
# <a name="fact-function"></a>Функция фактов

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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



## <a name="example"></a>Пример

Следующий фрагмент Q # завершится ошибкой:

```qsharp
Fact(false, "Expected true.");
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Diagnostics. противоречит](xref:Microsoft.Quantum.Diagnostics.Contradiction)