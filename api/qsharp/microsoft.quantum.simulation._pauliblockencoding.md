---
uid: Microsoft.Quantum.Simulation._PauliBlockEncoding
title: Функция _PauliBlockEncoding
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 6ad3e692f68ec2d405e19a7e467ef8fe33d449fc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225573"
---
# <a name="_pauliblockencoding-function"></a><span data-ttu-id="a5bec-102">Функция _PauliBlockEncoding</span><span class="sxs-lookup"><span data-stu-id="a5bec-102">_PauliBlockEncoding function</span></span>

<span data-ttu-id="a5bec-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="a5bec-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="a5bec-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a5bec-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a5bec-105">Создает единое блочное кодирование для Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="a5bec-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="a5bec-106">Хамилтониан $H = \ sum_ {j} \ alpha_j P_j $ описывается суммой Паулиных терминов $P _j $, каждый с действительным коэффициентом $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="a5bec-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function _PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem, statePrepUnitary : (Double[] -> (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)), multiplexer : ((Int, (Int -> (Qubit[] => Unit is Adj + Ctl))) -> ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="a5bec-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a5bec-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="a5bec-108">Женераторсистем: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="a5bec-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="a5bec-109">Объект `GeneratorSystem` , описывающий $H $ как сумму паулиных терминов</span><span class="sxs-lookup"><span data-stu-id="a5bec-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>


### <a name="stateprepunitary--double---littleendian--unit--is-adj--ctl"></a><span data-ttu-id="a5bec-110">статепрепунитари: [Double](xref:microsoft.quantum.lang-ref.double)[]-> [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [ед](xref:microsoft.quantum.lang-ref.unit)  .</span><span class="sxs-lookup"><span data-stu-id="a5bec-110">statePrepUnitary : [Double](xref:microsoft.quantum.lang-ref.double)[] -> [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a5bec-111">Единая операция $V $, которая применяет единое $V _j $ под управлением индекса $ \кет{ж} $, учитывая функцию $f: ж\ригхтарров V_j $.</span><span class="sxs-lookup"><span data-stu-id="a5bec-111">A unitary operation $V$ that applies the unitary $V_j$ controlled on index $\ket{j}$, given a function $f: j\rightarrow V_j$.</span></span>


### <a name="multiplexer--intint---qubit--unit--is-adj--ctl---littleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="a5bec-112">Мультиплексор: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL") — > ([литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="a5bec-112">multiplexer : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl) -> ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>





## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="a5bec-113">Выходные данные: ([Double](xref:microsoft.quantum.lang-ref.double),[блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="a5bec-113">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="a5bec-114">Первый параметр</span><span class="sxs-lookup"><span data-stu-id="a5bec-114">First parameter</span></span>

<span data-ttu-id="a5bec-115">Один из норм коэффициентов $ \алфа = \ sum_ {j} | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="a5bec-115">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="a5bec-116">Второй параметр</span><span class="sxs-lookup"><span data-stu-id="a5bec-116">Second parameter</span></span>

<span data-ttu-id="a5bec-117">`BlockEncodingReflection`Единое $U $ хамилтониан $U $.</span><span class="sxs-lookup"><span data-stu-id="a5bec-117">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $U$.</span></span> <span data-ttu-id="a5bec-118">Так как это единое значение соответствует $U ^ 2 = I $, это также отражение.</span><span class="sxs-lookup"><span data-stu-id="a5bec-118">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5bec-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5bec-119">Remarks</span></span>

<span data-ttu-id="a5bec-120">Примерами операций подготовка и отменяющая подготовка состояния $ \ sum_ {j} \скрт{\ alpha_j/\алфа}\кет{ж} $ и создание единого с учетом умножения <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .</span><span class="sxs-lookup"><span data-stu-id="a5bec-120">Example operations the prepare and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and construct a multiply-controlled unitary are <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>