---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualL
title: Функция Греатерсанорекуалл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualL
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: f33a7f17f3391d87e3eff9fb31939586036e83f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815840"
---
# <a name="greaterthanorequall-function"></a>Функция Греатерсанорекуалл

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает значение true только в том случае, если число больше или равно другому числу.

```qsharp
function GreaterThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Первое сравниваемое значение.


### <a name="b--bigint"></a>б: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Второе сравниваемое значение.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` значение и, только если `a` значение больше или равно `b` .

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```qsharp
let cond = a >= b;
let cond = GreaterThanOrEqualL(a, b);
```