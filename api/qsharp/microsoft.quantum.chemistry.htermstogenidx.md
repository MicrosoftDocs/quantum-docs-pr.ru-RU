---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: Функция Хтермстоженидкс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: 84dc132528f8fd1c45fb2f7345111a05626ee686
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839632"
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