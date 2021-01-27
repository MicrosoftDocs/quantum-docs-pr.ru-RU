---
uid: Microsoft.Quantum.Convert.Call
title: Операция вызова
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 93458d08aa83ffa8b7b33de8bf51c970af291db9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850196"
---
# <a name="call-operation"></a>Операция вызова

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Вызывает функцию с заданным входным параметром.

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a>Описание

При наличии функции и входных данных для этой функции вызывает функцию и возвращает ее выходные данные.

## <a name="input"></a>Входные данные

### <a name="fn--input---output"></a>FN: "входные данные >"

Вызываемая функция.


### <a name="input--input"></a>входные данные: "входные данные

Входные данные, передаваемые в функцию.



## <a name="output--output"></a>Выходные данные: "Output

Результат вызова метода `fn`.

## <a name="type-parameters"></a>Параметры типа

### <a name="input"></a>' Input


### <a name="output"></a>' Output



## <a name="remarks"></a>Remarks

Эта операция в основном полезна для принудительного вызова функции в определенном месте операции или для вызова функции, в которой ожидается операция.