---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZero
title: Операция Апплифзеро
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZero
qsharp.summary: ''
ms.openlocfilehash: 867e2e78ea787c2376fb2b1dcc6c72694fe08621
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230911"
---
# <a name="applyifzero-operation"></a>Операция Апплифзеро

Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)




```qsharp
operation ApplyIfZero<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit), zeroArg : 'T)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="measurementresult--__invalidresult__"></a>Меасурементресулт: __недопустимо <Result>__




### <a name="onresultzeroop--t--unit"></a>Онресултзеруп: 'T = [единица](xref:microsoft.quantum.lang-ref.unit)> 




### <a name="zeroarg--t"></a>Зероарг: 'T





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

