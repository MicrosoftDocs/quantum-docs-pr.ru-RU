---
uid: Microsoft.Quantum.Logical.EqualB
title: Функция Екуалб
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 2a15a749f52fe814db4fa57118f69c80fa22158a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817257"
---
# <a name="equalb-function"></a>Функция Екуалб

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает значение true только в том случае, если два входных значения равны.

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--bool"></a>ответ. [bool](xref:microsoft.quantum.lang-ref.bool)

Первое сравниваемое значение.


### <a name="b--bool"></a>б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение

Второе сравниваемое значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` Если и, только если `a` равно `b` .

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```qsharp
let cond = a == b;
let cond = EqualB(a, b);
```