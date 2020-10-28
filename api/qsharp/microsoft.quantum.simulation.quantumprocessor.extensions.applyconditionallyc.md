---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyC
title: Операция Аппликондитионаллик
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyC
qsharp.summary: ''
ms.openlocfilehash: fc1cf50b7befd40cf20720032329438715a9b856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730896"
---
# <a name="applyconditionallyc-operation"></a>Операция Аппликондитионаллик

Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Пакеты [](https://nuget.org/packages/)




```qsharp
operation ApplyConditionallyC<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="measurementresults--__invalidresult__"></a>Меасурементресултс: __Недопустимый <Result>__ []




### <a name="resultsvalues--__invalidresult__"></a>Ресултсвалуес: __Недопустимый <Result>__ []




### <a name="onequalop--t--unit-ctl"></a>Онекуалоп: 'T = список CTL для [единицы](xref:microsoft.quantum.lang-ref.unit)>




### <a name="equalarg--t"></a>Екуаларг: 'T




### <a name="onnonequalop--u--unit-ctl"></a>Оннонекуалоп: "U = список доверия для [единицы](xref:microsoft.quantum.lang-ref.unit)>




### <a name="nonequalarg--u"></a>Нонекуаларг: ' U





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U

