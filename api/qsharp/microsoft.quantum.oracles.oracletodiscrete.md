---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Функция Ораклетодискрете
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: ab59cdf0ab05092a9d4e7856b7808b13df655571
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842537"
---
# <a name="oracletodiscrete-function"></a>Функция Ораклетодискрете

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии операции, представляющей "черный ящик" Oracle, возвращает отдельную репликацию Oracle, которая представляет "черный ящик", повторяющийся несколько раз.

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a>Входные данные

### <a name="blackboxoracle--qubit--unit--is-adj--ctl"></a>Блаккбоксоракле: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Возведен операция.



## <a name="output--discreteoracle"></a>Выходные данные: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Операция частично применена к "черному ящику" Oracle, представляющему Дискретное время Oracle

## <a name="example"></a>Пример

`OracleToDiscrete(U)(3, target)` эквивалентно `U(target)` повторяется три раза.