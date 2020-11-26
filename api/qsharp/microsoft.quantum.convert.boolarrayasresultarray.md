---
uid: Microsoft.Quantum.Convert.BoolArrayAsResultArray
title: Функция Буларрайасресултаррай
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsResultArray
qsharp.summary: Converts a `Bool[]` type to a `Result[]` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: 388fb67ba33810fc813fb646577bfa7f4a2b51ae
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224468"
---
# <a name="boolarrayasresultarray-function"></a>Функция Буларрайасресултаррай

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Преобразует `Bool[]` тип в `Result[]` тип, где `true` сопоставляется с `One` и `false` сопоставляется с `Zero` .

```qsharp
function BoolArrayAsResultArray (input : Bool[]) : Result[]
```


## <a name="input"></a>Входные данные

### <a name="input--bool"></a>входные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]

`Bool[]` для преобразования.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__[]

Объект типа `Result[]`, представляющий объект `input`.