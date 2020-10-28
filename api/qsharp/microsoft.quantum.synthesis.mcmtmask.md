---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Определяемый пользователем тип Мкмтмаск
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 0d3ca12d55fa4b5e8332d50939954de29e39b715
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92734073"
---
# <a name="mcmtmask-user-defined-type"></a><span data-ttu-id="2a3ee-102">Определяемый пользователем тип Мкмтмаск</span><span class="sxs-lookup"><span data-stu-id="2a3ee-102">MCMTMask user defined type</span></span>

<span data-ttu-id="2a3ee-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="2a3ee-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="2a3ee-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2a3ee-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2a3ee-105">Тип для представления многоцелевого шлюза Тоффоли с несколькими управляемыми.</span><span class="sxs-lookup"><span data-stu-id="2a3ee-105">A type to represent a multiple-controlled multiple-target Toffoli gate.</span></span>

<span data-ttu-id="2a3ee-106">Первое целое число является битовой маской для управляющих линий.</span><span class="sxs-lookup"><span data-stu-id="2a3ee-106">The first integer is a bit mask for control lines.</span></span>  <span data-ttu-id="2a3ee-107">Битовые индексы, которые установлены в соответствии с индексами строк управления.</span><span class="sxs-lookup"><span data-stu-id="2a3ee-107">Bit indexes which are set correspond to control line indexes.</span></span>

<span data-ttu-id="2a3ee-108">Второе целое число является битовой маской для целевых строк.</span><span class="sxs-lookup"><span data-stu-id="2a3ee-108">The second integer is a bit mask for target lines.</span></span>  <span data-ttu-id="2a3ee-109">Битовые индексы, которые заданы, соответствуют индексам целевой строки.</span><span class="sxs-lookup"><span data-stu-id="2a3ee-109">Bit indexes which are set correspond to target line indexes.</span></span>

<span data-ttu-id="2a3ee-110">Битовые индексы обоих целых чисел должны быть несвязанными.</span><span class="sxs-lookup"><span data-stu-id="2a3ee-110">The bit indexes of both integers must be disjoint.</span></span>

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a><span data-ttu-id="2a3ee-111">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="2a3ee-111">Named Items</span></span>

### <a name="controlmask--int"></a><span data-ttu-id="2a3ee-112">Контролмаск: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a3ee-112">ControlMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="targetmask--int"></a><span data-ttu-id="2a3ee-113">Таржетмаск: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a3ee-113">TargetMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

