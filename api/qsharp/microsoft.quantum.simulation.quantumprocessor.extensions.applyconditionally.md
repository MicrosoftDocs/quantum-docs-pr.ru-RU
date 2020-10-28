---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionally
title: Операция Аппликондитионалли
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionally
qsharp.summary: ''
ms.openlocfilehash: fe623b240e35ee88f673b6e90db6307ef701d049
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710539"
---
# <a name="applyconditionally-operation"></a>Операция Аппликондитионалли

Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Пакеты [](https://nuget.org/packages/)




```qsharp
operation ApplyConditionally<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit), equalArg : 'T), (onNonEqualOp : ('U => Unit), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="measurementresults--__invalidresult__"></a>Меасурементресултс: __Недопустимый <Result>__ []




### <a name="resultsvalues--__invalidresult__"></a>Ресултсвалуес: __Недопустимый <Result>__ []




### <a name="onequalop--t--unit"></a>Онекуалоп: 'T = [единица](xref:microsoft.quantum.lang-ref.unit)> 




### <a name="equalarg--t"></a>Екуаларг: 'T




### <a name="onnonequalop--u--unit"></a>Оннонекуалоп: "U = [единица](xref:microsoft.quantum.lang-ref.unit)> 




### <a name="nonequalarg--u"></a>Нонекуаларг: ' U





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U

