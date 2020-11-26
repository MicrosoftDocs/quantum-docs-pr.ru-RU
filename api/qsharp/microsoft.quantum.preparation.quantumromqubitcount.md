---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: Функция Куантумромкубиткаунт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: >-
  > [!WARNING]

  > QuantumROMQubitCount has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> instead.


  Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: 0ec1e042b9f675505f73bfcdcc6706d0bc0367df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210409"
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