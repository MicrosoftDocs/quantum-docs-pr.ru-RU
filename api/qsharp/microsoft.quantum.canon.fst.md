---
uid: Microsoft.Quantum.Canon.Fst
title: Функция ФСТ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 634f11881a054df7fe79d889832ea6bd80a7394f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206941"
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