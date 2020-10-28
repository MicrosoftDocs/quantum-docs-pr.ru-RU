---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: Функция Куантумромкубиткаунт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: 988d5efa3e27cf5e9a276ab3ab443c10f88fe1ad
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732608"
---
# <a name="quantumromqubitcount-function"></a><span data-ttu-id="965fd-102">Функция Куантумромкубиткаунт</span><span class="sxs-lookup"><span data-stu-id="965fd-102">QuantumROMQubitCount function</span></span>

<span data-ttu-id="965fd-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="965fd-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="965fd-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="965fd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="965fd-105">Возвращает общее число Кубитс, которые должны быть выделены операции, возвращенной `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="965fd-105">Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.</span></span>

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a><span data-ttu-id="965fd-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="965fd-106">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="965fd-107">Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="965fd-107">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="965fd-108">Целевая ошибка $ \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="965fd-108">The target error $\epsilon$.</span></span>


### <a name="ncoeffs--int"></a><span data-ttu-id="965fd-109">Нкоеффс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="965fd-109">nCoeffs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="965fd-110">Количество коэффициентов, указанных в `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="965fd-110">Number of coefficients specified in `QuantumROM`.</span></span>



## <a name="output--intintint"></a><span data-ttu-id="965fd-111">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="965fd-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int)))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="965fd-112">Первый параметр</span><span class="sxs-lookup"><span data-stu-id="965fd-112">First parameter</span></span>

<span data-ttu-id="965fd-113">Кортеж, `(x,(y,z))` где `x = y + z` — Общее число выделенных Кубитс, `y` — число Кубитс для `LittleEndian` регистра, а `z` — число Кубитс мусора.</span><span class="sxs-lookup"><span data-stu-id="965fd-113">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>