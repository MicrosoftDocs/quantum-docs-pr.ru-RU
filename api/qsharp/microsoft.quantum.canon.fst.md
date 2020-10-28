---
uid: Microsoft.Quantum.Canon.Fst
title: Функция ФСТ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 88ff5e29de9eeefcc1e207f277c37c63cb0faade
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716182"
---
# <a name="fst-function"></a>Функция ФСТ

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


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