---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Функция Функтионасоператион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 90e9f0c922a77fbb6d6faf8945d4f5d1c8ff33b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713508"
---
# <a name="functionasoperation-function"></a>Функция Функтионасоператион

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакеты [](https://nuget.org/packages/)


Преобразует функции в операции.

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a>Описание

При наличии функции возвращает операцию, которая вызывает эту функцию и не выполняет никаких других действий.

## <a name="input"></a>Входные данные

### <a name="fn--input---output"></a>FN: "входные данные >"

Функция, которую необходимо преобразовать в операцию.



## <a name="output--input--output"></a>Выходные данные: input => ' Output 

Операция `op` , которая `op(input)` идентична для `fn(input)` All `input` .

## <a name="type-parameters"></a>Параметры типа

### <a name="input"></a>' Input

Тип входных данных функции для преобразования.
### <a name="output"></a>' Output

Тип выходных данных функции для преобразования.

## <a name="remarks"></a>Remarks

Это в основном полезно для передачи функций функциям или операциям, которые в качестве входных данных ожидает операцию.