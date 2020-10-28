---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: Функция Статеораклефромдетерминистикстатеоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: ccb083dbaaec2f306ba0740ef364ebb22408ed98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733344"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a>Функция Статеораклефромдетерминистикстатеоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакеты [](https://nuget.org/packages/)


Преобразует Oracle типа `DeterministicStateOracle` в `StateOracle` .

```qsharp
function StateOracleFromDeterministicStateOracle (deterministicStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.StateOracle
```


## <a name="input"></a>Входные данные

### <a name="deterministicstateoracle--deterministicstateoracle"></a>Детерминистикстатеоракле: [детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Подготовка состояния Oracle $A $ типа `DeterministicStateOracle` .



## <a name="output--stateoracle"></a>Выходные данные: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)

То же состояние подготовки Oracle $A $, но теперь типа `StateOracle` . Обратите внимание, что индекс флага в этом `StateOracle` случае является фиктивной переменной и не имеет результата.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Oracle. Детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Microsoft. тактов. Oracle. Статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)