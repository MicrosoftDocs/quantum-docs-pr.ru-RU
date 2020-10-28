---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Функция _IdentityTimeDependentGeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 0b440ce9adaab562e16b02da46844c68a7470b11
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710693"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a>Функция _IdentityTimeDependentGeneratorSystem

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакеты [](https://nuget.org/packages/)


Возвращает систему генератора, совместимую с Хамилтониан `H(s) = 0` , где `s` — параметр расписания.

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Входные данные

### <a name="schedule--double"></a>Расписание: [Double](xref:microsoft.quantum.lang-ref.double)

Эти входные данные игнорируются и определяются для согласованности с <xref:microsoft.quantum.canon.timedependentgeneratorsystem> определяемым пользователем типом.



## <a name="output--generatorsystem"></a>Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Система генератора, представляющая развитие в Хамилтониан $H (s) = $0 для всех $s $.