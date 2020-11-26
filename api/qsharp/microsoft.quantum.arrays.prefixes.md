---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Функция префиксов
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 3501c11437534b1623bffba272a4517487e5634a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220400"
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