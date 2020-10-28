---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: Функция Висзероинсертедат
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 6e13251741dadb19740b208cdfc13a14964a48dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733880"
---
# <a name="withzeroinsertedat-function"></a>Функция Висзероинсертедат

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакеты [](https://nuget.org/packages/)


Вставить 0-разрядное значение в целое число

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a>Описание

Эта операция принимает целое число, вставляет 0 в бит `position` и возвращает обновленное значение в виде целого числа.  Например, при вставке значения 0 в позиции 2 в номере 10 (10 долл. {10} = 1010_ {2} $) возвращается число 18 ($18 _ {10} = 10010_ {2} $).

## <a name="input"></a>Входные данные

### <a name="position--int"></a>Расположение: [int](xref:microsoft.quantum.lang-ref.int)

Позиции, в которую вставляется 0


### <a name="value--int"></a>значение: [int](xref:microsoft.quantum.lang-ref.int)

Изменяемое значение



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Измененное значение