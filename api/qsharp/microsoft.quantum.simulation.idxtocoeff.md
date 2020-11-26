---
uid: Microsoft.Quantum.Simulation.IdxToCoeff
title: Функция Идкстокоефф
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdxToCoeff
qsharp.summary: Used in implementation of `PauliBlockEncoding`
ms.openlocfilehash: 4e10b61e56b791a39841385ec79893c1392b9563
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225131"
---
# <a name="idxtocoeff-function"></a>Функция Идкстокоефф

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Используется в реализации `PauliBlockEncoding`

```qsharp
function IdxToCoeff (idx : Int, genFun : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), genIdxToCoeff : (Microsoft.Quantum.Simulation.GeneratorIndex -> Double)) : Double
```


## <a name="input"></a>Входные данные

### <a name="idx--int"></a>IDX: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="genfun--int---generatorindex"></a>женфун: [int](xref:microsoft.quantum.lang-ref.int) -> [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)




### <a name="genidxtocoeff--generatorindex---double"></a>женидкстокоефф: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex) -> [double](xref:microsoft.quantum.lang-ref.double)





## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Паулиблоккенкодинг](xref:Microsoft.Quantum.Simulation.PauliBlockEncoding)