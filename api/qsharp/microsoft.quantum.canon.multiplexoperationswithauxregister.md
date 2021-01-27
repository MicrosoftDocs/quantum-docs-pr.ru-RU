---
uid: Microsoft.Quantum.Canon.MultiplexOperationsWithAuxRegister
title: Операция Мултиплексоператионсвисауксрегистер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsWithAuxRegister
qsharp.summary: Implementation step of MultiplexOperations.
ms.openlocfilehash: 91db22d6261709c1c3506c80ff600c904748575a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852458"
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