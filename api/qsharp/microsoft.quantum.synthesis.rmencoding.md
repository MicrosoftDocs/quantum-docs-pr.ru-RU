---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: Функция Рменкодинг
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: a506ccb637b331a392ea75383c8bd605114af059
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202946"
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