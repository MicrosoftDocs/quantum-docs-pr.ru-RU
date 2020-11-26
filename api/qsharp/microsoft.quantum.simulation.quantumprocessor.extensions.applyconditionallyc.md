---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyC
title: Операция Аппликондитионаллик
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyC
qsharp.summary: ''
ms.openlocfilehash: 963a85e0e442592c01a2e70fa0dc02d6048d8be7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229041"
---
# <a name="applyconditionallyc-operation"></a>Операция Аппликондитионаллик

Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)




```qsharp
operation ApplyConditionallyC<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl), nonEqualArg : 'U)) : Unit is Ctl
```


## <a name="input"></a>Входные данные

### <a name="measurementresults--__invalidresult__"></a>Меасурементресултс: __Недопустимый <Result>__[]




### <a name="resultsvalues--__invalidresult__"></a>Ресултсвалуес: __Недопустимый <Result>__[]




### <a name="onequalop--t--unit--is-ctl"></a>Онекуалоп: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL




### <a name="equalarg--t"></a>Екуаларг: 'T




### <a name="onnonequalop--u--unit--is-ctl"></a>Оннонекуалоп: "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL




### <a name="nonequalarg--u"></a>Нонекуаларг: ' U





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U

