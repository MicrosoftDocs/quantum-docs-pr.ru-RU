---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRCA
title: Операция Апплифелсерка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRCA
qsharp.summary: ''
ms.openlocfilehash: fb2f7ded44708a93d97d7041bf15be2c8c48990a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730697"
---
# <a name="applyifelserca-operation"></a>Операция Апплифелсерка

Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Пакеты [](https://nuget.org/packages/)




```qsharp
operation ApplyIfElseRCA<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj + Ctl), zeroArg : 'T), (onResultOneOp : ('U => Unit is Adj + Ctl), oneArg : 'U)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="measurementresult--__invalidresult__"></a>Меасурементресулт: __недопустимо <Result>__




### <a name="onresultzeroop--t--unit-adj--ctl"></a>Онресултзеруп: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL




### <a name="zeroarg--t"></a>Зероарг: 'T




### <a name="onresultoneop--u--unit-adj--ctl"></a>Онресултонеоп: "U => [единицы](xref:microsoft.quantum.lang-ref.unit) + CTL




### <a name="onearg--u"></a>Онеарг: ' U





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U

