---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Операция Естиматетермекспектатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 7df4c1ea859140a669698434c6f8a786ea3bc2ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835668"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="eceed-102">Операция Естиматетермекспектатион</span><span class="sxs-lookup"><span data-stu-id="eceed-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="eceed-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="eceed-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="eceed-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="eceed-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="eceed-105">Вычисление энергии, связанной с заданным Jordan-Wignerным термином Хамилтониан</span><span class="sxs-lookup"><span data-stu-id="eceed-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="eceed-106">Описание</span><span class="sxs-lookup"><span data-stu-id="eceed-106">Description</span></span>

<span data-ttu-id="eceed-107">Эта операция оценивает значение ожидания, связанное с каждым оператором измерения, и умножает его на соответствующий коэффициент, используя выборку.</span><span class="sxs-lookup"><span data-stu-id="eceed-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="eceed-108">Результаты объединяются в переменную, содержащую энергию Jordan-Wigner термина.</span><span class="sxs-lookup"><span data-stu-id="eceed-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="eceed-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="eceed-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit--is-adj"></a><span data-ttu-id="eceed-110">Инпутстатеунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) ></span><span class="sxs-lookup"><span data-stu-id="eceed-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="eceed-111">Единое значение, используемое для подготовки состояния.</span><span class="sxs-lookup"><span data-stu-id="eceed-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="eceed-112">Ops: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="eceed-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="eceed-113">Операторы измерения Jordan-Wigner термина.</span><span class="sxs-lookup"><span data-stu-id="eceed-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="eceed-114">коеффс: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="eceed-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="eceed-115">Коэффициенты Jordan-Wignerного термина.</span><span class="sxs-lookup"><span data-stu-id="eceed-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="eceed-116">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eceed-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eceed-117">Число Кубитс, необходимое для имитации системы молекулярное.</span><span class="sxs-lookup"><span data-stu-id="eceed-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="eceed-118">Нсамплес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eceed-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eceed-119">Количество выборок для оценки условия использования.</span><span class="sxs-lookup"><span data-stu-id="eceed-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="eceed-120">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="eceed-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="eceed-121">Энергия, связанная с Jordan-Wignerным термином.</span><span class="sxs-lookup"><span data-stu-id="eceed-121">The energy associated to the Jordan-Wigner term.</span></span>