---
uid: Microsoft.Quantum.Canon.Fst
title: Функция ФСТ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: cd5746358c8323f8d2dbca44965fa5dbac0a84c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840514"
---
# <a name="fst-function"></a>Функция ФСТ

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии пары возвращает ее первый элемент.

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a>Входные данные

### <a name="pair--tu"></a>пара: ('T, ' U)

Кортеж с двумя элементами.



## <a name="output--t"></a>Выходные данные: 'T

Первый элемент объекта `pair`.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип первого элемента пары.
### <a name="u"></a>' U

Тип второго члена пары.