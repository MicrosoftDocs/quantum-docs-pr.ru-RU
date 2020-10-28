---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: Функция Таржетстатерефлектионоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: a6ed0397be57ef6f14a712749cc416e1fd98b71c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731920"
---
# <a name="targetstatereflectionoracle-function"></a>Функция Таржетстатерефлектионоракле

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакеты [](https://nuget.org/packages/)


Конструирует `ReflectionOracle` о целевом состоянии, уникально помеченном флагом кубит.

Целевое состояние имеет одно значение кубит, равное 1, и все остальные 0: $ \кет {1} _f $.

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a>Входные данные

### <a name="idxflagqubit--int"></a>Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)

Индекс, помечающий кубит $f $ of Oracle.



## <a name="output--reflectionoracle"></a>Выходные данные: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Значение типа `ReflectionOracle` , которое отражает состояние, отмеченное параметром $ \кет {1} _f $.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Рефлектионоракле](xref:Microsoft.Quantum.Canon.ReflectionOracle)