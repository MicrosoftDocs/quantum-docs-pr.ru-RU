---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: Функция Куантумромкубиткаунт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: >-
  > [!WARNING]

  > QuantumROMQubitCount has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> instead.


  Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: d6eac64eb62ec7a88d3231249b0bb1e05818f6e6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856794"
---
# <a name="quantumromqubitcount-function"></a>Функция Куантумромкубиткаунт

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> Куантумромкубиткаунт является устаревшим. Взамен рекомендуется использовать <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements>.

Возвращает общее число Кубитс, которые должны быть выделены операции, возвращенной `QuantumROM` .

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a>Входные данные

### <a name="targeterror--double"></a>Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)

Целевая ошибка $ \епсилон $.


### <a name="ncoeffs--int"></a>Нкоеффс: [int](xref:microsoft.quantum.lang-ref.int)

Количество коэффициентов, указанных в `QuantumROM` .



## <a name="output--intintint"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))

## <a name="first-parameter"></a>Первый параметр

Кортеж, `(x,(y,z))` где `x = y + z` — Общее число выделенных Кубитс, `y` — число Кубитс для `LittleEndian` регистра, а `z` — число Кубитс мусора.