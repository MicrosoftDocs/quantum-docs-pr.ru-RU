---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: Функция Детерминистикстатеораклефромстатеоракле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: 183b1108ead6239e26bb0b38144cb9374e7bf285
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226763"
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