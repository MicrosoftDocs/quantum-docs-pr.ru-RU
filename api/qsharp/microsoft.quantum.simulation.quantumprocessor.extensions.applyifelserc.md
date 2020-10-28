---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRC
title: Операция Апплифелсерк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRC
qsharp.summary: ''
ms.openlocfilehash: 21069c43c16bc9712973ac4e0afea8320c0d83a9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709462"
---
# <a name="applyifelserc-operation"></a>Операция Апплифелсерк

Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Пакеты [](https://nuget.org/packages/)




```qsharp
operation ApplyIfElseRC<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T), (onResultOneOp : ('U => Unit is Ctl), oneArg : 'U)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="measurementresult--__invalidresult__"></a>Меасурементресулт: __недопустимо <Result>__




### <a name="onresultzeroop--t--unit-ctl"></a>Онресултзеруп: 'T = список CTL для [единицы](xref:microsoft.quantum.lang-ref.unit)>




### <a name="zeroarg--t"></a>Зероарг: 'T




### <a name="onresultoneop--u--unit-ctl"></a>Онресултонеоп: "U = список доверия для [единицы](xref:microsoft.quantum.lang-ref.unit)>




### <a name="onearg--u"></a>Онеарг: ' U





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U

