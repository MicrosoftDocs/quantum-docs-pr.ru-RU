---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Функция _IdentityTimeDependentGeneratorSystem
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 7b93a6674bec974e61496696a3d8403225b16d80
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225607"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="67111-102">Функция _IdentityTimeDependentGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="67111-102">_IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="67111-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="67111-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="67111-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="67111-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="67111-105">Возвращает систему генератора, совместимую с Хамилтониан `H(s) = 0` , где `s` — параметр расписания.</span><span class="sxs-lookup"><span data-stu-id="67111-105">Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.</span></span>

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="67111-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="67111-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="67111-107">Расписание: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="67111-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="67111-108">Эти входные данные игнорируются и определяются для согласованности с <xref:microsoft.quantum.canon.timedependentgeneratorsystem> определяемым пользователем типом.</span><span class="sxs-lookup"><span data-stu-id="67111-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.canon.timedependentgeneratorsystem> user-defined type.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="67111-109">Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="67111-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="67111-110">Система генератора, представляющая развитие в Хамилтониан $H (s) = $0 для всех $s $.</span><span class="sxs-lookup"><span data-stu-id="67111-110">A generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>