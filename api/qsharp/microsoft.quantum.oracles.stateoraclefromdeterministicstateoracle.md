---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: Функция Статеораклефромдетерминистикстатеоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: 4eed29072cab9e8c106509a6a114c8a071441079
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842503"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a>Функция Статеораклефромдетерминистикстатеоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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