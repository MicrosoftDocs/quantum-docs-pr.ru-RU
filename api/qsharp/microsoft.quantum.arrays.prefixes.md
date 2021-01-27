---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Функция префиксов
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: a2e1721f8f59bf9aa425f04710637023d482a2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845510"
---
# <a name="prefixes-function"></a>Функция префиксов

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива возвращает все его префиксы.

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a>Описание

Возвращает массив всех префиксов, начиная с массива, у которого есть только первый элемент, вплоть до полного массива.

## <a name="input"></a>Входные данные

### <a name="array--t"></a>массив: 'T []

Массив элементов.



## <a name="output--t"></a>Выходные данные: 'T [] []



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип `array` элементов.

## <a name="example"></a>Пример

```qsharp
let prefixes = Prefixes([23, 42, 144]);
// prefixes = [[23], [23, 42], [23, 42, 144]]
```