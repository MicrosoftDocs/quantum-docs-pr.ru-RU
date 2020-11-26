---
uid: Microsoft.Quantum.Simulation._AddGeneratorSystems
title: Функция _AddGeneratorSystems
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: ffb635d7cb6c388c2158b7adb6bb872b0c77cdb1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229755"
---
# <a name="_addgeneratorsystems-function"></a>Функция _AddGeneratorSystems

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="remarks"></a>Комментарии

Это промежуточный шаг, и его не следует вызывать.