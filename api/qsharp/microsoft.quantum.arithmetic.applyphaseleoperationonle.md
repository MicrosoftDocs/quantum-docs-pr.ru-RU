---
uid: Microsoft.Quantum.Arithmetic.ApplyPhaseLEOperationOnLE
title: Операция Апплифаселеоператиононле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyPhaseLEOperationOnLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.
ms.openlocfilehash: d94fdb55e051e76dd518eff14b80d1a24516bf8a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843675"
---
# <a name="applyphaseleoperationonle-operation"></a>Операция Апплифаселеоператиононле

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию, которая принимает <xref:microsoft.quantum.arithmetic.littleendian> регистрацию в качестве входных данных для целевого регистра типа <xref:microsoft.quantum.arithmetic.phaselittleendian> .

```qsharp
operation ApplyPhaseLEOperationOnLE (op : (Microsoft.Quantum.Arithmetic.PhaseLittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--phaselittleendian--unit"></a>Op: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Операция, которая будет применена.


### <a name="target--littleendian"></a>Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр, к которому применяется операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Регистр преобразуется в `PhaseLittleEndian` с помощью <xref:microsoft.quantum.canon.qftle> и возвращается в исходное представление после применения `op` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплифаселеоператиононлеа](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [Microsoft. тактов. Canon. Апплифаселеоператиононлеа](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [Microsoft. тактов. Canon. Апплифаселеоператиононлека](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA)