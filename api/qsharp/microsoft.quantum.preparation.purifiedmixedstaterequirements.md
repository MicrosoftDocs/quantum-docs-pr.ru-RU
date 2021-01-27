---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: Функция Пурифиедмикседстатерекуирементс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 6ddb48ba66eea87a07d515ff791bfb34f2d98b76
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856833"
---
# <a name="purifiedmixedstaterequirements-function"></a>Функция Пурифиедмикседстатерекуирементс

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает общее число Кубитс, которые должны быть выделены для применения операции, возвращенной @"microsoft.quantum.preparation.purifiedmixedstate" .

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a>Входные данные

### <a name="targeterror--double"></a>Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)

Целевая ошибка $ \епсилон $.


### <a name="ncoefficients--int"></a>НкоеффиЦиентс: [int](xref:microsoft.quantum.lang-ref.int)

Число коэффициентов, которые должны быть указаны при подготовке смешанного состояния.



## <a name="output--mixedstatepreparationrequirements"></a>Выходные данные: [микседстатепрепаратионрекуирементс](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)

Описание того, сколько Кубитс требуется в целом, и для каждого индекса и регистров мусора, используемых @"microsoft.quantum.preparation.purifiedmixedstate" функцией.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. подготовка. Пурифиедмикседстате](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)