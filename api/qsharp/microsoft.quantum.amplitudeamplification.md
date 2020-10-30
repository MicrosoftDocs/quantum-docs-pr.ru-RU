---
uid: Microsoft.Quantum.AmplitudeAmplification
title: Пространство имен Microsoft. тактов. Амплитудеамплификатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: namespace
qsharp.name: Microsoft.Quantum.AmplitudeAmplification
qsharp.summary: This namespace contains functions and operations for performing amplitude amplification.
ms.openlocfilehash: 09c29bd9d0648bb8652051ad97ceca6ef6557df3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731985"
---
# <a name="microsoftquantumamplitudeamplification-namespace"></a><span data-ttu-id="d9974-102">Пространство имен Microsoft. тактов. Амплитудеамплификатион</span><span class="sxs-lookup"><span data-stu-id="d9974-102">Microsoft.Quantum.AmplitudeAmplification namespace</span></span>

<span data-ttu-id="d9974-103">Это пространство имен содержит функции и операции для выполнения усиления амплитуды.</span><span class="sxs-lookup"><span data-stu-id="d9974-103">This namespace contains functions and operations for performing amplitude amplification.</span></span>



## <a name="description"></a><span data-ttu-id="d9974-104">Описание</span><span class="sxs-lookup"><span data-stu-id="d9974-104">Description</span></span>

<span data-ttu-id="d9974-105">Усиление амплитуды очевидным с частичными отражениями — это наиболее Общая форма реализации усиления амплитуды.</span><span class="sxs-lookup"><span data-stu-id="d9974-105">Oblivious amplitude amplification with partial reflections is the most general form of amplitude amplification implemented here.</span></span>

<span data-ttu-id="d9974-106">Это вызывается с помощью операции Ампампобливиаусбирефлектионфасес.</span><span class="sxs-lookup"><span data-stu-id="d9974-106">This is called through the operation AmpAmpObliviousByReflectionPhases.</span></span>

<span data-ttu-id="d9974-107">Он имеет два регистра: `ancillaRegister` и `systemRegister` .</span><span class="sxs-lookup"><span data-stu-id="d9974-107">This has two registers: `ancillaRegister` and `systemRegister`.</span></span>

<span data-ttu-id="d9974-108">Это принимает две Oracle для этих отражений типа `ReflectionOracle` , которые работают только с `ancillaRegister` регистром.</span><span class="sxs-lookup"><span data-stu-id="d9974-108">This accepts two oracles for these reflections of type `ReflectionOracle` which act only on the `ancillaRegister` register.</span></span>

<span data-ttu-id="d9974-109">При этом принимается специальное значение Oracle для очевиднымности амплитуды типа `ObliviousOracle` , который работает совместно с обеими регистрами.</span><span class="sxs-lookup"><span data-stu-id="d9974-109">This accepts an oracle special to oblivious amplitude amplification of type `ObliviousOracle` which acts jointly on both register.</span></span>

<span data-ttu-id="d9974-110">Предполагается, что входное состояние `ancillaRegister` — это уникальный $-$1 еиженстате первого оператора отражения $I-2 \ Сисакет {s} \ неверное {s} $.</span><span class="sxs-lookup"><span data-stu-id="d9974-110">The input state to `ancillaRegister` is assumed to be the unique $-1$ eigenstate of the first reflection operator $I - 2\ket{s}\bra{s}$.</span></span>

<span data-ttu-id="d9974-111">Отражения, связанные с состоянием целевого такта, часто реализуются при условии доступа к Oracle, который подготавливает это состояние от вычислительной базы $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="d9974-111">Reflections about a target quantum state are often implemented by assuming access to an oracle that prepare that state from the computational basis $\ket{0\cdots 0}$.</span></span>

<span data-ttu-id="d9974-112">Для нашего соглашения для этих Oracle требуется два регистра: один кубит `flagQubit` регистр и регистр для всех остальных элементов регистра анЦилларегистер.</span><span class="sxs-lookup"><span data-stu-id="d9974-112">Our convention for these oracles requires two registers: a single-qubit `flagQubit` register, and a register for everything else on the ancillaRegister register.</span></span>

<span data-ttu-id="d9974-113">Oracle типа `StateOracle` работает совместно с обоими регистрами для создания целевого состояния, помеченного $ \кет {1} $ в `flagQubit` регистре, с некоторой реальной амплитудой.</span><span class="sxs-lookup"><span data-stu-id="d9974-113">The oracle of type `StateOracle` acts jointly on both registers to create the target state flagged by $\ket{1}$ in the `flagQubit` register with some real amplitude.</span></span>

<span data-ttu-id="d9974-114">Отражение `ReflectionOracle` о состоянии этого флага создается операцией `TargetStateReflectionOracle` .</span><span class="sxs-lookup"><span data-stu-id="d9974-114">The reflection `ReflectionOracle` about the this flag state is generated by the operation `TargetStateReflectionOracle`.</span></span>

<span data-ttu-id="d9974-115">Отражение `ReflectionOracle` состояния ввода `ancillaRegister` создается инвертированным статеоракле, а затем отразится около $ \ket{0\cdots 0} $ с рефлектионстарт ().</span><span class="sxs-lookup"><span data-stu-id="d9974-115">The reflection `ReflectionOracle` about the input state to `ancillaRegister` is generated by the inverting StateOracle and then reflecting about $\ket{0\cdots 0}$ with ReflectionStart().</span></span>

<span data-ttu-id="d9974-116">Oracle типа `DeterministicStateOracle` обрабатывает `qubitState` регистры для создания целевого состояния точно без флага.</span><span class="sxs-lookup"><span data-stu-id="d9974-116">The oracle of type `DeterministicStateOracle` acts on the `qubitState` registers to create the target state exactly with no flag.</span></span>

<span data-ttu-id="d9974-117">`AmpAmpObliviousByOraclePhases` — Это версия усиления амплитуды очевидным, которая принимает Oracle `StateOracle` и `ObliviousOracle` вместо отражения.</span><span class="sxs-lookup"><span data-stu-id="d9974-117">`AmpAmpObliviousByOraclePhases` is a version of oblivious amplitude amplification that accepts oracles `StateOracle` and `ObliviousOracle` instead of reflections.</span></span>

<span data-ttu-id="d9974-118">Обратите внимание, что усиление амплитуды является особым случаем для очевидныма амплитуды `ObliviousOracle` , где является оператором идентификации, и отсутствует системный Кубитс, т. е. `systemRegister` пустой.</span><span class="sxs-lookup"><span data-stu-id="d9974-118">Note that amplitude amplification is a special case of oblivious amplitude amplification where `ObliviousOracle` is the identity operator, and there are no system qubits i.e. `systemRegister` is empty.</span></span>

<span data-ttu-id="d9974-119">Это вызывается с помощью операции `AmpAmByReflectionPhases` и `AmpAmpByOraclePhases` .</span><span class="sxs-lookup"><span data-stu-id="d9974-119">This is called through the operation `AmpAmByReflectionPhases` and `AmpAmpByOraclePhases`.</span></span>

<span data-ttu-id="d9974-120">Этапы частичной отражения в стандартном случае поиска Гровер предоставляются функцией Ампампфасесстандард.</span><span class="sxs-lookup"><span data-stu-id="d9974-120">The phases for partial reflections in the standard case of Grover search is provided by the function AmpAmpPhasesStandard.</span></span>

<span data-ttu-id="d9974-121">Например, у нас есть следующие зависимости: Ампампбйоракле-> Ампампбйораклефасес-> Ампампобливиаусбйораклефасес-> Ампампобливиаусбирефлектионфасес.</span><span class="sxs-lookup"><span data-stu-id="d9974-121">For instance, we have the following dependencies: AmpAmpByOracle -> AmpAmpByOraclePhases -> AmpAmpObliviousByOraclePhases -> AmpAmpObliviousByReflectionPhases.</span></span>