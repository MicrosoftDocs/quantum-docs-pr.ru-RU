---
uid: Microsoft.Quantum.Canon.LogicalANDMeasAndFix
title: Операция Логикаландмеасандфикс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: LogicalANDMeasAndFix
qsharp.summary: Computes the logical AND of multiple qubits.
ms.openlocfilehash: 86e4b9a8c6ed5f4f56db0ceefc8051d34e911c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715929"
---
# <a name="logicalandmeasandfix-operation"></a>Операция Логикаландмеасандфикс

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Вычисление логического и для нескольких Кубитс.

```qsharp
operation LogicalANDMeasAndFix (ctrlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a>Входные данные

### <a name="ctrlregister--qubit"></a>Ктрлрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубитс входные данные для нескольких входных и многоэлементных шлюзов.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, в который записывается вывод и. Предполагается, что всегда начинается в состоянии $ \кет {0} $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Если `ctrlRegister` имеет ровно $2 $ Кубитс, это эквивалентно операции, `CCNOT` но этапу $e ^ {i \ PI/2} $ on $ \кет {001} $ и $-e ^ {i \ PI/2} $ on $ \кет {101} $ and $ \кет {011} $.
Смежная функция также является подходом меры и адресной привязки, которая является инверсией исходной операции только в особых случаях (см. ссылки), но использует меньше T-шлюзов.

## <a name="references"></a>Ссылки

- [*Крейг гиднэй* , 1709,06648](https://arxiv.org/abs/1709.06648)