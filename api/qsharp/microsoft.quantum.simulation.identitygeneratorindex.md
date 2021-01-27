---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: Функция Идентитиженераториндекс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: b389ca1e0737463e6ccd5ce885b849c6b32d65d1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844341"
---
# <a name="identitygeneratorindex-function"></a><span data-ttu-id="ebeba-102">Функция Идентитиженераториндекс</span><span class="sxs-lookup"><span data-stu-id="ebeba-102">IdentityGeneratorIndex function</span></span>

<span data-ttu-id="ebeba-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ebeba-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ebeba-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ebeba-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ebeba-105">Возвращает индекс генератора, совместимый с нулевым Хамилтониан, `H = 0` который соответствует операции эволюции идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="ebeba-105">Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.</span></span>

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="ebeba-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ebeba-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="ebeba-107">Идкстерм: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ebeba-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ebeba-108">Эти входные данные игнорируются и определяются для согласованности с <xref:microsoft.quantum.simulation.generatorsystem> определяемым пользователем типом.</span><span class="sxs-lookup"><span data-stu-id="ebeba-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.simulation.generatorsystem> user-defined type.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="ebeba-109">Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="ebeba-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="ebeba-110">Индекс генератора, представляющий развитие в Хамилтониан $H = $0.</span><span class="sxs-lookup"><span data-stu-id="ebeba-110">A generator index representing evolution under the Hamiltonian $H = 0$.</span></span>