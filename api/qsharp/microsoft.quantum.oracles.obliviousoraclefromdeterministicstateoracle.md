---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: Функция Обливиаусораклефромдетерминистикстатеоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: 9e18776ad4d6adf0068213117c6d1d8ed5c5f126
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732201"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a>Функция Обливиаусораклефромдетерминистикстатеоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакеты [](https://nuget.org/packages/)


Объединяет Oracle `DeterministicStateOracle` и `ObliviousOracle` .

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a>Входные данные

### <a name="ancillaoracle--deterministicstateoracle"></a>АнЦиллаоракле: [детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Подготовка состояния Oracle $A $ типа, `DeterministicStateOracle` действующего на register $a $.


### <a name="signaloracle--obliviousoracle"></a>Сигналоракле: [обливиаусоракле](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Тип Oracle $U $ of `ObliviousOracle` , который взаимодействует с register $a, s $.



## <a name="output--obliviousoracle"></a>Выходные данные: [обливиаусоракле](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Oracle $O = UA $ of Type `ObliviousOracle` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Oracle. Детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Microsoft. тактов. Oracle. Обливиаусоракле](xref:Microsoft.Quantum.Oracles.ObliviousOracle)