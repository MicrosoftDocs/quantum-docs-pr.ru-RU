---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyA
title: Операция Аппликондитионалля
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyA
qsharp.summary: ''
ms.openlocfilehash: b6f7e7d6d51e531b0ec9e7e4f2f5772038421933
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710526"
---
# <a name="applyconditionallya-operation"></a>Операция Аппликондитионалля

Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Пакеты [](https://nuget.org/packages/)




```qsharp
operation ApplyConditionallyA<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Adj), equalArg : 'T), (onNonEqualOp : ('U => Unit is Adj), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="measurementresults--__invalidresult__"></a>Меасурементресултс: __Недопустимый <Result>__ []




### <a name="resultsvalues--__invalidresult__"></a>Ресултсвалуес: __Недопустимый <Result>__ []




### <a name="onequalop--t--unit-adj"></a>Онекуалоп: 'T [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода




### <a name="equalarg--t"></a>Екуаларг: 'T




### <a name="onnonequalop--u--unit-adj"></a>Оннонекуалоп: "U [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода




### <a name="nonequalarg--u"></a>Нонекуаларг: ' U





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U

