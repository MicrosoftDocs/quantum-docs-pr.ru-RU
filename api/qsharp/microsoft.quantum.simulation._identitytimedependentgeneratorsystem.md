---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Функция _IdentityTimeDependentGeneratorSystem
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 960842f50353c01362f90eb38d979fb7c4f15d9a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857990"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a>Функция _IdentityTimeDependentGeneratorSystem

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает систему генератора, совместимую с Хамилтониан `H(s) = 0` , где `s` — параметр расписания.

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Входные данные

### <a name="schedule--double"></a>Расписание: [Double](xref:microsoft.quantum.lang-ref.double)

Эти входные данные игнорируются и определяются для согласованности с <xref:microsoft.quantum.canon.timedependentgeneratorsystem> определяемым пользователем типом.



## <a name="output--generatorsystem"></a>Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Система генератора, представляющая развитие в Хамилтониан $H (s) = $0 для всех $s $.