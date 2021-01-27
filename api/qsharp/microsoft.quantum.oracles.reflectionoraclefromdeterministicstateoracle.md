---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: Функция Рефлектионораклефромдетерминистикстатеоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c260bdbcdb2ce53ad602bf84e0d31ef4fec24a79
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842525"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a>Функция Рефлектионораклефромдетерминистикстатеоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Конструирует отражение о заданном состоянии из Oracle.

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a>Описание

Учитывая детерминированное состояние подготовка Oracle, представленная единой матрицей $O $, результатом этой функции является Oracle, который применяет отражение состояния $ \кет{\пси} $, подготовленного Oracle $O $; то есть, состояние $ \кет{\пси} $, например, $O \кет {0} = \кет{\пси} $.

## <a name="input"></a>Входные данные

### <a name="oracle--deterministicstateoracle"></a>Oracle: [детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Объект Oracle, подготавливающий копии состояния $ \кет{\пси} $.



## <a name="output--reflectionoracle"></a>Выходные данные: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

База данных Oracle, отражающая состояние $ \кет{\пси} $.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Oracle. Детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Microsoft. тактов. Oracle. Рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)