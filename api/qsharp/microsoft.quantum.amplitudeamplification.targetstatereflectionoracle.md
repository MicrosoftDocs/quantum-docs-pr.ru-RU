---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: Функция Таржетстатерефлектионоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 4169ccf3e210e27f779311553b845ea04f2c7dc6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843893"
---
# <a name="targetstatereflectionoracle-function"></a>Функция Таржетстатерефлектионоракле

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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