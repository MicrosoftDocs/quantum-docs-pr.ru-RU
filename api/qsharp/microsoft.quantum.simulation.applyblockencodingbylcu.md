---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Операция Апплиблоккенкодингбилку
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 1575b93b6c3242e1dffafb330c44cc017a72a8b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732145"
---
# <a name="applyblockencodingbylcu-operation"></a>Операция Апплиблоккенкодингбилку

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакеты [](https://nuget.org/packages/)


Реализация метода `BlockEncodingByLCU`.

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit
```


## <a name="input"></a>Входные данные

### <a name="statepreparation--t--unit-adj--ctl"></a>Статепрепаратион: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL




### <a name="selector--ts--unit-adj--ctl"></a>селектор: ('T) [=>ная](xref:microsoft.quantum.lang-ref.unit) расгода и список доверия




### <a name="auxiliary--t"></a>вспомогательная: 'T




### <a name="system--s"></a>система:





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="s"></a>Возникл

