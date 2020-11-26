---
uid: Microsoft.Quantum.Canon.MultiplexOperationsWithAuxRegister
title: Операция Мултиплексоператионсвисауксрегистер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsWithAuxRegister
qsharp.summary: Implementation step of MultiplexOperations.
ms.openlocfilehash: 530e78ba0c5ce6e0627177527daf2ccc56f537eb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205989"
---
# <a name="multiplexoperationswithauxregister-operation"></a>Операция Мултиплексоператионсвисауксрегистер

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Шаг реализации Мултиплексоператионс.

```qsharp
operation MultiplexOperationsWithAuxRegister<'T> (unitaries : ('T => Unit is Adj + Ctl)[], auxillaryRegister : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="unitaries--t--unit--is-adj--ctl"></a>унитариес: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL []"




### <a name="auxillaryregister--qubit"></a>Ауксилларирегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="index--littleendian"></a>Индекс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)




### <a name="target--t"></a>Целевой объект: 'T





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Мултиплексоператионс](xref:Microsoft.Quantum.Canon.MultiplexOperations)