---
uid: Microsoft.Quantum.Convert.BoolArrayAsResultArray
title: Функция Буларрайасресултаррай
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsResultArray
qsharp.summary: Converts a `Bool[]` type to a `Result[]` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: b30da07272ee1a6c19ae13afa618ba5deb7aaa2d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834191"
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