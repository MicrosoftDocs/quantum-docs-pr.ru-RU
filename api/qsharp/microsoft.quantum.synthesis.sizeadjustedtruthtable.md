---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: Функция Сизеаджустедтрустабле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: 8d69aa119c25a0f64743fec36c00ecdef2450c44
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855319"
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