---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: Функция Сизеаджустедтрустабле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: c53ac3f2c46bca955847fc7b380337e3910390ac
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202929"
---
# <a name="sizeadjustedtruthtable-function"></a>Функция Сизеаджустедтрустабле

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Корректирует таблицу истинности из массива логических значений в соответствии с количеством переменных

Новый массив возвращается длиной `2^numVars` , возможно, требуется расширить `table` размер с помощью `false` записей или усечь его до `2^numVars` элементов.

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a>Входные данные

### <a name="table--bool"></a>Таблица: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Истинная таблица как массив значений истинности


### <a name="numvars--int"></a>Нумварс: [int](xref:microsoft.quantum.lang-ref.int)

Число переменных



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Таблица скорректированных размеров