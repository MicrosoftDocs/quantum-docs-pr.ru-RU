---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Операция Естиматетермекспектатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: ef689c55f966e63a2ab8bcdccf99d9cb5e6d3a4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713731"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="b8980-102">Операция Естиматетермекспектатион</span><span class="sxs-lookup"><span data-stu-id="b8980-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="b8980-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="b8980-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="b8980-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b8980-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b8980-105">Вычисление энергии, связанной с заданным Jordan-Wignerным термином Хамилтониан</span><span class="sxs-lookup"><span data-stu-id="b8980-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="b8980-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b8980-106">Description</span></span>

<span data-ttu-id="b8980-107">Эта операция оценивает значение ожидания, связанное с каждым оператором измерения, и умножает его на соответствующий коэффициент, используя выборку.</span><span class="sxs-lookup"><span data-stu-id="b8980-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="b8980-108">Результаты объединяются в переменную, содержащую энергию Jordan-Wigner термина.</span><span class="sxs-lookup"><span data-stu-id="b8980-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="b8980-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b8980-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit-adj"></a><span data-ttu-id="b8980-110">Инпутстатеунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="b8980-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="b8980-111">Единое значение, используемое для подготовки состояния.</span><span class="sxs-lookup"><span data-stu-id="b8980-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="b8980-112">Ops: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="b8980-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="b8980-113">Операторы измерения Jordan-Wigner термина.</span><span class="sxs-lookup"><span data-stu-id="b8980-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="b8980-114">коеффс: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b8980-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b8980-115">Коэффициенты Jordan-Wignerного термина.</span><span class="sxs-lookup"><span data-stu-id="b8980-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="b8980-116">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b8980-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b8980-117">Число Кубитс, необходимое для имитации системы молекулярное.</span><span class="sxs-lookup"><span data-stu-id="b8980-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="b8980-118">Нсамплес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b8980-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b8980-119">Количество выборок для оценки условия использования.</span><span class="sxs-lookup"><span data-stu-id="b8980-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="b8980-120">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b8980-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b8980-121">Энергия, связанная с Jordan-Wignerным термином.</span><span class="sxs-lookup"><span data-stu-id="b8980-121">The energy associated to the Jordan-Wigner term.</span></span>