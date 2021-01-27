---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Функция _IdentityTimeDependentGeneratorSystem
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 960842f50353c01362f90eb38d979fb7c4f15d9a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857990"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="16fde-102">Функция _IdentityTimeDependentGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="16fde-102">_IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="16fde-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="16fde-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="16fde-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="16fde-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="16fde-105">Возвращает систему генератора, совместимую с Хамилтониан `H(s) = 0` , где `s` — параметр расписания.</span><span class="sxs-lookup"><span data-stu-id="16fde-105">Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.</span></span>

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="16fde-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="16fde-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="16fde-107">Расписание: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="16fde-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="16fde-108">Эти входные данные игнорируются и определяются для согласованности с <xref:microsoft.quantum.canon.timedependentgeneratorsystem> определяемым пользователем типом.</span><span class="sxs-lookup"><span data-stu-id="16fde-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.canon.timedependentgeneratorsystem> user-defined type.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="16fde-109">Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="16fde-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="16fde-110">Система генератора, представляющая развитие в Хамилтониан $H (s) = $0 для всех $s $.</span><span class="sxs-lookup"><span data-stu-id="16fde-110">A generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>