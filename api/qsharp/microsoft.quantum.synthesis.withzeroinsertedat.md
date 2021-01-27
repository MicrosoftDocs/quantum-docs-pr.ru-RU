---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: Функция Висзероинсертедат
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 7d5f8838b6ae555524fb0e82e14f93e6c77e43d4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855197"
---
# <a name="withzeroinsertedat-function"></a>Функция Висзероинсертедат

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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