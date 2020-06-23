---
title: Примеры приложений для квантовой химии
description: Изучите примеры приложений библиотеки квантовой химии от Майкрософт
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples
ms.openlocfilehash: 5168fc8592d34a32ba67e5a0c4793aa17599fd35
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85273933"
---
# <a name="quantum-chemistry-examples"></a><span data-ttu-id="3cdb9-103">Примеры из квантовой химии</span><span class="sxs-lookup"><span data-stu-id="3cdb9-103">Quantum chemistry examples</span></span>

<span data-ttu-id="3cdb9-104">В статье о концепциях квантовой химии описано, как вручную создать гамильтоново представление фермиона.</span><span class="sxs-lookup"><span data-stu-id="3cdb9-104">In the quantum chemistry concepts, we manually constructed example fermion Hamiltonians.</span></span> <span data-ttu-id="3cdb9-105">Теперь мы применим к нему алгоритмы химического моделирования, описанные в статье о [моделировании гамильтоновой динамики](xref:microsoft.quantum.libraries.standard.algorithms), [квантовую оценку фазы](xref:microsoft.quantum.libraries.characterization) из библиотеки canon.</span><span class="sxs-lookup"><span data-stu-id="3cdb9-105">We now combine the chemistry simulation algorithms outlined in [Simulating Hamiltonian dynamics](xref:microsoft.quantum.libraries.standard.algorithms) with [quantum phase estimation](xref:microsoft.quantum.libraries.characterization) in the canon library.</span></span> <span data-ttu-id="3cdb9-106">Такое сочетание позволит получить оценки энергетических уровней в молекуле, выраженной в нашем представлении, а это и есть одно из важнейших применений квантовой химии на квантовом компьютере.</span><span class="sxs-lookup"><span data-stu-id="3cdb9-106">This combination allows us to obtain  estimates of energy levels in the represented molecule, which is one of the key applications of quantum chemistry on a quantum computer.</span></span> 

<span data-ttu-id="3cdb9-107">Мы не будем указывать гамильтоновы функции по одной, а сразу рассмотрим готовые примеры, которые позволят выполнять масштабные эксперименты с квантовой химией.</span><span class="sxs-lookup"><span data-stu-id="3cdb9-107">Instead of specifying terms of the Hamiltonian one-by-one, we also work through some examples that allow us to perform quantum chemistry experiments at scale.</span></span> <span data-ttu-id="3cdb9-108">Сначала мы рассмотрим примеры, которые загружают гамильтоново представление химического вещества в формате [схемы Брумбриджа](xref:microsoft.quantum.libraries.chemistry.schema.broombridge).</span><span class="sxs-lookup"><span data-stu-id="3cdb9-108">We begin with examples that load a chemistry Hamiltonian encoded in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge).</span></span>

<span data-ttu-id="3cdb9-109">С молекулами, которые слишком велики для [симулятора полного состояния](xref:microsoft.quantum.machines.full-state-simulator), тоже можно выполнять интересные эксперименты.</span><span class="sxs-lookup"><span data-stu-id="3cdb9-109">For molecules that are too large to simulate on the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), interesting science can still be performed.</span></span> <span data-ttu-id="3cdb9-110">Например, [симулятор трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) позволяет оценить затраты ресурсов на выполнение масштабного химического моделирования.</span><span class="sxs-lookup"><span data-stu-id="3cdb9-110">For instance, the resource costs of performing large chemistry simulations may still be evaluated by targeting the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>

<span data-ttu-id="3cdb9-111">Мы продемонстрируем вам интересные возможности библиотеки химического моделирования на нескольких готовых примерах.</span><span class="sxs-lookup"><span data-stu-id="3cdb9-111">Let us now illustrate interesting applications of the chemistry simulation library through a few of the provided samples.</span></span>
