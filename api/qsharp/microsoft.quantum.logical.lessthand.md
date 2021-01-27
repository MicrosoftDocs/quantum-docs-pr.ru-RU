---
uid: Microsoft.Quantum.Logical.LessThanD
title: Функция Лесссанд
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanD
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 7135ed4b3414d143f5020496ae524bf89980a8a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849158"
---
# <a name="lessthand-function"></a>Функция Лесссанд

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает значение true только в том случае, если число меньше, чем другое число.

```qsharp
function LessThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--double"></a>ответ. [Double](xref:microsoft.quantum.lang-ref.double)

Первое сравниваемое значение.


### <a name="b--double"></a>б: [двойной](xref:microsoft.quantum.lang-ref.double)

Второе сравниваемое значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` Если и, только если `a` является строго меньшим `b` .

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```qsharp
let cond = a < b;
let cond = LessThanD(a, b);
```