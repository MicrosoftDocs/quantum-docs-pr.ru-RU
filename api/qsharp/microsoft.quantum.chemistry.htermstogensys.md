---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: Функция Хтермстоженсис
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: 3d5963b8751a22d7116d6c1cf094d89e1d6b556f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851764"
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