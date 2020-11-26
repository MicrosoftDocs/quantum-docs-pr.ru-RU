---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: Функция Хтермстоженсис
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: 936e1bcc58b2f1af3bdb606884128c38d2f58867
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204119"
---
# <a name="htermstogensys-function"></a>Функция Хтермстоженсис

Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Преобразует Хамилтониан в `HTerm[]` формате данных в женераторсистем.

```qsharp
function HTermsToGenSys (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Входные данные

### <a name="data--hterm"></a>данные: [хтерм](xref:Microsoft.Quantum.Chemistry.HTerm)[]

Входные данные в `HTerm[]` формате.


### <a name="termtype--int"></a>Термтипе: [int](xref:microsoft.quantum.lang-ref.int)[]

Дополнительные сведения, добавленные в Женераториндекс.



## <a name="output--generatorsystem"></a>Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Объект Женераторсистем, представляющий Хамилтониан, представленный входными данными `data` .