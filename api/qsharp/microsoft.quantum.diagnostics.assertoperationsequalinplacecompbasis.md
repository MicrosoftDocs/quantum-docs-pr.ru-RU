---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlaceCompBasis
title: Операция Ассертоператионсекуалинплацекомпбасис
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlaceCompBasis
qsharp.summary: Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis. This is a necessary, but not sufficient, condition for the equality of two unitaries.
ms.openlocfilehash: 3275680f86ca2a178c7f044b97d226fe41c3186c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712962"
---
# <a name="assertoperationsequalinplacecompbasis-operation"></a>Операция Ассертоператионсекуалинплацекомпбасис

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Проверяет, равен ли операция `givenU` операции `expectedU` с заданным размером входных данных, проверяя действие операций только на векторах от вычислительной основе.
Это обязательное, но недостаточное условие для равенства двух унитариес.

```qsharp
operation AssertOperationsEqualInPlaceCompBasis (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс $n $, с которыми работают операции `givenU` `expectedU` .


### <a name="givenu--qubit--unit"></a>Гивену: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция с $n $ Кубитс будет проверена.


### <a name="expectedu--qubit--unit-adj"></a>Експектеду: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода

Операция ссылки на $n $ Кубитс `givenU` для сравнения с.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

