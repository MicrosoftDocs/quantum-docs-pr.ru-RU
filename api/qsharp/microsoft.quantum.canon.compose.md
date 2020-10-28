---
uid: Microsoft.Quantum.Canon.Compose
title: Функция создания
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 02cff7eef4d55d27d5d72e6219a90b7d8f5beb3b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716490"
---
# <a name="compose-function"></a>Функция создания

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


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