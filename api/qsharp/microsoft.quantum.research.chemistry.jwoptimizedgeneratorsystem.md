---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedGeneratorSystem
title: Функция Жвоптимизедженераторсистем
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: 13e3386a612b238c29a9e3368eed8628e8ed9b66
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847016"
---
# <a name="jwoptimizedgeneratorsystem-function"></a>Функция Жвоптимизедженераторсистем

Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)

Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Преобразует Хамилтониан, описанный в `JWOptimizedHTerms` `GeneratorSystem` выражении, в терминах `GeneratorIndex` соглашения, определенного в этом файле.

```qsharp
function JWOptimizedGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Входные данные

### <a name="data--jwoptimizedhterms"></a>данные: [жвоптимизедхтермс](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)

Описание Хамилтониан в `JWOptimizedHTerms` формате.



## <a name="output--generatorsystem"></a>Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Представление Хамилтониан как `GeneratorSystem` .