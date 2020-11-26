---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: Функция Хтермстоженидкс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: dbe0718fa3b5439a2987d455fdad73731c988678
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216019"
---
# <a name="htermstogenidx-function"></a>Функция Хтермстоженидкс

Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Преобразует индекс в Хамилтониан термин в `HTerm[]` формате данных в женераториндекс.

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Входные данные

### <a name="data--hterm"></a>данные: [хтерм](xref:Microsoft.Quantum.Chemistry.HTerm)[]

Входные данные в `HTerm[]` формате.


### <a name="termtype--int"></a>Термтипе: [int](xref:microsoft.quantum.lang-ref.int)[]

Дополнительные сведения, добавленные в Женераториндекс.


### <a name="idx--int"></a>IDX: [int](xref:microsoft.quantum.lang-ref.int)

Индекс в термине Хамилтониан



## <a name="output--generatorindex"></a>Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Женераториндекс, представляющий Хамилтониан термин, представленный `data[idx]` вместе с дополнительными сведениями, добавленными `termType` .