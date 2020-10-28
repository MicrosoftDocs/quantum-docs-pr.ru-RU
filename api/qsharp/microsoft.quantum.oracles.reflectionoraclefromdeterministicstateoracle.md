---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: Функция Рефлектионораклефромдетерминистикстатеоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c2d37216aebcdc5243d0f1d6ec9db261cc9bd0c8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732177"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a>Функция Рефлектионораклефромдетерминистикстатеоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакеты [](https://nuget.org/packages/)


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