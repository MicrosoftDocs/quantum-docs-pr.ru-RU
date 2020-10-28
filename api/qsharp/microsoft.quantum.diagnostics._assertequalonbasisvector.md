---
uid: Microsoft.Quantum.Diagnostics._assertEqualOnBasisVector
title: _assertEqualOnBasisVector операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _assertEqualOnBasisVector
qsharp.summary: Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same. The basis state is described by `basis` parameter. See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.
ms.openlocfilehash: 01b6d5aede102e47df86ea70d071d81eba1ade6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713157"
---
# <a name="_assertequalonbasisvector-operation"></a>_assertEqualOnBasisVector операция

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Проверяет, совпадает ли результат применения двух операций `givenU` и `expectedU` с состоянием основания. Состояние основания описывается `basis` параметром.
<xref:microsoft.quantum.extensions.fliptobasis>Дополнительные сведения об этом описании см. в разделе функция.

```qsharp
operation _assertEqualOnBasisVector (basis : Int[], givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="basis--int"></a>Базис: [int](xref:microsoft.quantum.lang-ref.int)[]

Состояние основания, заданное ИДЕНТИФИКАТОРом однокубитного состояния (0 <= ID <= 3) для каждого из $n $ Кубитс.


### <a name="givenu--qubit--unit"></a>Гивену: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция с $n $ Кубитс будет проверена.


### <a name="expectedu--qubit--unit-adj"></a>Експектеду: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода

Операция ссылки на $n $ Кубитс, для которой требуется сравнить Гивену.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

