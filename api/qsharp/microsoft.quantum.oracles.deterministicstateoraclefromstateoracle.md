---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: Функция Детерминистикстатеораклефромстатеоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: af545a7d6e82e654ee36ab3ba77c8f8be3384b96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854559"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a>Функция Детерминистикстатеораклефромстатеоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Преобразует Oracle типа `StateOracle` в `DeterministicStateOracle` .

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a>Входные данные

### <a name="idxflagqubit--int"></a>Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)

Индекс для флага `stateOracle` $A кубит $, который явно работает с двумя регистрами: флаг $f $ и system $s $, например $A \кет {0} \_ ф\кет {\ PSI} \_ s $.


### <a name="stateoracle--stateoracle"></a>Статеоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)

Подготовка состояния Oracle $A $ типа `StateOracle` .



## <a name="output--deterministicstateoracle"></a>Выходные данные: [детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Одно и то же состояние подготовленная база данных Oracle $A $, но теперь `DeterministicStateOracle` имеет тип, поэтому он работает с регистром, где $a, s $ больше не разделяются явным образом, например  $A \ket{0\psi} \_ {as} $.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Oracle. Статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)
- [Microsoft. тактов. Oracle. Детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)