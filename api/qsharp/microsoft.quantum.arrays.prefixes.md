---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Функция префиксов
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 1576e57e9dc64a605eb65cb841640e72a3b126ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730064"
---
# <a name="prefixes-function"></a>Функция префиксов

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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