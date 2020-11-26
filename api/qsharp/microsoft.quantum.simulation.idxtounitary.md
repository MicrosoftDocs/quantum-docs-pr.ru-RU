---
uid: Microsoft.Quantum.Simulation.IdxToUnitary
title: Функция Идкстаунитари
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdxToUnitary
qsharp.summary: Used in implementation of `PauliBlockEncoding`
ms.openlocfilehash: dd13b2d2e846dcddb820599ea26aa25b90903dbd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229279"
---
# <a name="idxtounitary-function"></a>Функция Идкстаунитари

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Используется в реализации `PauliBlockEncoding`

```qsharp
function IdxToUnitary (idx : Int, genFun : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), genIdxToUnitary : (Microsoft.Quantum.Simulation.GeneratorIndex -> (Qubit[] => Unit is Adj + Ctl))) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="idx--int"></a>IDX: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="genfun--int---generatorindex"></a>женфун: [int](xref:microsoft.quantum.lang-ref.int) -> [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)




### <a name="genidxtounitary--generatorindex---qubit--unit--is-adj--ctl"></a>женидкстаунитари: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex) -> [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"





## <a name="output--qubit--unit--is-adj--ctl"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Паулиблоккенкодинг](xref:Microsoft.Quantum.Simulation.PauliBlockEncoding)