---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Функция Функтионасоператион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: cf4f8c97bf38b3a64eb952d0a502bc21c29c579c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833839"
---
# <a name="functionasoperation-function"></a>Функция Функтионасоператион

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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