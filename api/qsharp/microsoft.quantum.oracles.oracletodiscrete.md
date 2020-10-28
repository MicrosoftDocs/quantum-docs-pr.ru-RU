---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Функция Ораклетодискрете
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: d26d57c587f24e7f74102c12753bcddb00fd8a9d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733360"
---
# <a name="oracletodiscrete-function"></a>Функция Ораклетодискрете

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакеты [](https://nuget.org/packages/)


При наличии операции, представляющей "черный ящик" Oracle, возвращает отдельную репликацию Oracle, которая представляет "черный ящик", повторяющийся несколько раз.

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a>Входные данные

### <a name="blackboxoracle--qubit--unit-adj--ctl"></a>Блаккбоксоракле: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL

Возведен операция.



## <a name="output--discreteoracle"></a>Выходные данные: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Операция частично применена к "черному ящику" Oracle, представляющему Дискретное время Oracle