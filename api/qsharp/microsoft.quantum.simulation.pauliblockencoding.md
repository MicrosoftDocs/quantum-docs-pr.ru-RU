---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: Функция Паулиблоккенкодинг
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 2e37b40c60d19aa747114de988dddc19f0d7c50b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848008"
---
# <a name="pauliblockencoding-function"></a><span data-ttu-id="266e7-102">Функция Паулиблоккенкодинг</span><span class="sxs-lookup"><span data-stu-id="266e7-102">PauliBlockEncoding function</span></span>

<span data-ttu-id="266e7-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="266e7-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="266e7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="266e7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="266e7-105">Создает единое блочное кодирование для Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="266e7-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="266e7-106">Хамилтониан $H = \ sum_ {j} \ alpha_j P_j $ описывается суммой Паулиных терминов $P _j $, каждый с действительным коэффициентом $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="266e7-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="266e7-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="266e7-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="266e7-108">Женераторсистем: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="266e7-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="266e7-109">Объект `GeneratorSystem` , описывающий $H $ как сумму паулиных терминов</span><span class="sxs-lookup"><span data-stu-id="266e7-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>



## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="266e7-110">Выходные данные: ([Double](xref:microsoft.quantum.lang-ref.double),[блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="266e7-110">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="266e7-111">Первый параметр</span><span class="sxs-lookup"><span data-stu-id="266e7-111">First parameter</span></span>

<span data-ttu-id="266e7-112">Один из норм коэффициентов $ \алфа = \ sum_ {j} | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="266e7-112">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="266e7-113">Второй параметр</span><span class="sxs-lookup"><span data-stu-id="266e7-113">Second parameter</span></span>

<span data-ttu-id="266e7-114">`BlockEncodingReflection`Единое $U $ хамилтониан $H $.</span><span class="sxs-lookup"><span data-stu-id="266e7-114">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $H$.</span></span> <span data-ttu-id="266e7-115">Так как это единое значение соответствует $U ^ 2 = I $, это также отражение.</span><span class="sxs-lookup"><span data-stu-id="266e7-115">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="266e7-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="266e7-116">Remarks</span></span>

<span data-ttu-id="266e7-117">Это достигается путем подготовки и отменяя подготовку состояния $ \ sum_ {j} \скрт{\ alpha_j/\алфа}\кет{ж} $, а также конструирования единых <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> и <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .</span><span class="sxs-lookup"><span data-stu-id="266e7-117">This is obtained by preparing and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and constructing a multiply-controlled unitary <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>