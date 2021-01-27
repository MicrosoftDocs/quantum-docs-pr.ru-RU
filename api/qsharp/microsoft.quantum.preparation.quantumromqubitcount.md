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
# <a name="quantumromqubitcount-function"></a><span data-ttu-id="efeff-102">Функция Куантумромкубиткаунт</span><span class="sxs-lookup"><span data-stu-id="efeff-102">QuantumROMQubitCount function</span></span>

<span data-ttu-id="efeff-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="efeff-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="efeff-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="efeff-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="efeff-105">Куантумромкубиткаунт является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="efeff-105">QuantumROMQubitCount has been deprecated.</span></span> <span data-ttu-id="efeff-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements>.</span><span class="sxs-lookup"><span data-stu-id="efeff-106">Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> instead.</span></span>

<span data-ttu-id="efeff-107">Возвращает общее число Кубитс, которые должны быть выделены операции, возвращенной `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="efeff-107">Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.</span></span>

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a><span data-ttu-id="efeff-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="efeff-108">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="efeff-109">Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="efeff-109">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="efeff-110">Целевая ошибка $ \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="efeff-110">The target error $\epsilon$.</span></span>


### <a name="ncoeffs--int"></a><span data-ttu-id="efeff-111">Нкоеффс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="efeff-111">nCoeffs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="efeff-112">Количество коэффициентов, указанных в `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="efeff-112">Number of coefficients specified in `QuantumROM`.</span></span>



## <a name="output--intintint"></a><span data-ttu-id="efeff-113">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="efeff-113">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int)))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="efeff-114">Первый параметр</span><span class="sxs-lookup"><span data-stu-id="efeff-114">First parameter</span></span>

<span data-ttu-id="efeff-115">Кортеж, `(x,(y,z))` где `x = y + z` — Общее число выделенных Кубитс, `y` — число Кубитс для `LittleEndian` регистра, а `z` — число Кубитс мусора.</span><span class="sxs-lookup"><span data-stu-id="efeff-115">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>