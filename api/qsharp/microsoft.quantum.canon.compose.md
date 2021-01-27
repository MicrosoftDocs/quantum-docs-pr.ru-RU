---
uid: Microsoft.Quantum.Canon.Compose
title: Функция создания
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 73eab66e2e9a9af56d01db927eb7af38bb56a23e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840907"
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