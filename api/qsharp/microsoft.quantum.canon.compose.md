---
uid: Microsoft.Quantum.Canon.Compose
title: Функция создания
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: f8c6ad36220b48be1723c2d91cbf7c0a4947af14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216767"
---
# <a name="compose-function"></a>Функция создания

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает композицию двух функций.

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a>Описание

При наличии двух функций $f $ и $g $ возвращает новую функцию, представляющую $f \Цирк g $.

## <a name="input"></a>Входные данные

### <a name="outer--u---v"></a>Внешний: ' U-> ' V

Вторая функция, которая будет применена.


### <a name="inner--t---u"></a>внутренний: не> "U

Первая функция, которая будет применена.



## <a name="output--t---v"></a>Выходные данные: 'T-> ' V

Новая функция $h $ таким, что для всех входных данных $x $, $f (g (x)) = h (x) $.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных первой функции, которая должна быть применена.
### <a name="u"></a>' U

Тип выходных данных первой функции, которая будет применена, и тип входных данных второй функции.
### <a name="v"></a>"V

Тип выходных данных второй функции, которая будет применена.