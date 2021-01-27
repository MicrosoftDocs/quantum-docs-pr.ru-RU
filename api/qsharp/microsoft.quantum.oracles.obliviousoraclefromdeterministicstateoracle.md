---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: Функция Обливиаусораклефромдетерминистикстатеоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: c7aa80feda67d68216f318073ee8c6a5eb0653c0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854529"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a>Функция Обливиаусораклефромдетерминистикстатеоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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