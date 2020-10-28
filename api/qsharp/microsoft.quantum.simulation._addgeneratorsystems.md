---
uid: Microsoft.Quantum.Simulation._AddGeneratorSystems
title: Функция _AddGeneratorSystems
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: 3bce9faf229f3b1f683e060437ec08da795ef185
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710708"
---
# <a name="_addgeneratorsystems-function"></a>Функция _AddGeneratorSystems

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакеты [](https://nuget.org/packages/)


Добавляет две `GeneratorSystem` s для создания нового `GeneratorSystem` .

```qsharp
function _AddGeneratorSystems (idxTerm : Int, nTermsA : Int, nTermsB : Int, generatorIndexFunctionA : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), generatorIndexFunctionB : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Входные данные

### <a name="idxterm--int"></a>Идкстерм: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="ntermsa--int"></a>Нтермса: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="ntermsb--int"></a>Нтермсб: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="generatorindexfunctiona--int---generatorindex"></a>женераториндексфунктиона: [int](xref:microsoft.quantum.lang-ref.int) -> [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)




### <a name="generatorindexfunctionb--int---generatorindex"></a>женераториндексфунктионб: [int](xref:microsoft.quantum.lang-ref.int) -> [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)





## <a name="output--generatorindex"></a>Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)



## <a name="remarks"></a>Remarks

Это промежуточный шаг, и его не следует вызывать.