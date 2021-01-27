---
uid: Microsoft.Quantum.Logical.EqualD
title: Функция equaled
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: f8a24d7bfb9b4f7b8b0e1f68a94bfb341716b024
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98816865"
---
# <a name="equald-function"></a>Функция equaled

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает значение true только в том случае, если два входных значения равны.

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--double"></a>ответ. [Double](xref:microsoft.quantum.lang-ref.double)

Первое сравниваемое значение.


### <a name="b--double"></a>б: [двойной](xref:microsoft.quantum.lang-ref.double)

Второе сравниваемое значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` Если и, только если `a` равно `b` .

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```qsharp
let cond = a == b;
let cond = EqualD(a, b);
```