---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: Функция Рменкодинг
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: f3c54d2e40511dacb21618b4eaf1eef9f4903f9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855343"
---
# <a name="rmencoding-function"></a>Функция Рменкодинг

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


{-1,1} кодирование логического значения истинности

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a>Входные данные

### <a name="b--bool"></a>б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение

Логическое значение.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

1, если `b` имеет значение false, в противном случае — 1.