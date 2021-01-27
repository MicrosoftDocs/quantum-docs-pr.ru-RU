---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLECA
title: Операция Апплилеоператиононфаселека
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLECA
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: 024eb923d8e09ecb75a95dd61d300fd0d643c7ec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843737"
---
# <a name="applyleoperationonphaseleca-operation"></a>Операция Апплилеоператиононфаселека

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию, которая принимает <xref:microsoft.quantum.arithmetic.phaselittleendian> регистрацию в качестве входных данных для целевого регистра типа <xref:microsoft.quantum.arithmetic.littleendian> .

```qsharp
operation ApplyLEOperationOnPhaseLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="op--littleendian--unit--is-adj--ctl"></a>Op: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"

Операция, которая будет применена.


### <a name="target--phaselittleendian"></a>Целевой объект: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Регистр, к которому применяется операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Регистр преобразуется в `LittleEndian` с помощью <xref:microsoft.quantum.canon.qftle> и возвращается в исходное представление после применения `op` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплилеоператиононфаселе](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE)
- [Microsoft. тактов. Canon. Апплилеоператиононфаселеа](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA)
- [Microsoft. тактов. Canon. Апплилеоператиононфаселек](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC)