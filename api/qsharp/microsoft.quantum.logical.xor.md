---
uid: Microsoft.Quantum.Logical.Xor
title: Функция XOR
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: afb94bd1fd0b791a9a7d84bc28b0cc2baf9a0938
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197098"
---
# <a name="xor-function"></a>Функция XOR

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает логическое исключающее сложение двух значений.

```qsharp
function Xor (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--bool"></a>ответ. [bool](xref:microsoft.quantum.lang-ref.bool)

Первое значение, которое необходимо считать.


### <a name="b--bool"></a>б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение

Второе значение, которое необходимо считать.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` только в том случае, если только один из них `a` `b` имеет значение `true` .