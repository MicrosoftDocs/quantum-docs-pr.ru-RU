---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionally
title: Операция Аппликондитионалли
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionally
qsharp.summary: ''
ms.openlocfilehash: 24d52576d2fb3e83f294874be4b0d1cd6a80f188
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229075"
---
# <a name="applyconditionally-operation"></a>Операция Аппликондитионалли

Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)




```qsharp
operation ApplyConditionally<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit), equalArg : 'T), (onNonEqualOp : ('U => Unit), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="measurementresults--__invalidresult__"></a>Меасурементресултс: __Недопустимый <Result>__[]




### <a name="resultsvalues--__invalidresult__"></a>Ресултсвалуес: __Недопустимый <Result>__[]




### <a name="onequalop--t--unit"></a>Онекуалоп: 'T = [единица](xref:microsoft.quantum.lang-ref.unit)> 




### <a name="equalarg--t"></a>Екуаларг: 'T




### <a name="onnonequalop--u--unit"></a>Оннонекуалоп: "U = [единица](xref:microsoft.quantum.lang-ref.unit)> 




### <a name="nonequalarg--u"></a>Нонекуаларг: ' U





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U

