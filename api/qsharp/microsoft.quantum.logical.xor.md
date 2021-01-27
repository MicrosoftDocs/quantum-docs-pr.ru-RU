---
uid: Microsoft.Quantum.Logical.Xor
title: Функция XOR
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: 4a4af7f628ca64170e046584d9caffe7ceee3d56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848454"
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