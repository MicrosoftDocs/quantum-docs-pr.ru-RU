---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: Функция Хтермтоженидкс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: dd72355adb32f9a0d109ee36b24be2d445f3fa66
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714837"
---
# <a name="htermtogenidx-function"></a>Функция Хтермтоженидкс

Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)

Пакеты [](https://nuget.org/packages/)


Преобразует термин Хамилтониан в `HTerm` формате данных в женераториндекс.

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Входные данные

### <a name="term--hterm"></a>термин: [хтерм](xref:Microsoft.Quantum.Chemistry.HTerm)

Входные данные в `HTerm` формате.


### <a name="termtype--int"></a>Термтипе: [int](xref:microsoft.quantum.lang-ref.int)[]

Дополнительные сведения, добавленные в Женераториндекс.



## <a name="output--generatorindex"></a>Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Женераториндекс, представляющий Хамилтониан термин, представленный `term` вместе с дополнительными сведениями, добавленными `termType` .