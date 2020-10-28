---
uid: Microsoft.Quantum.Convert.Call
title: Операция вызова
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 8630f846b4b9823ce1c1dfd61dc8ca81e468517d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713535"
---
# <a name="call-operation"></a>Операция вызова

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакеты [](https://nuget.org/packages/)


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