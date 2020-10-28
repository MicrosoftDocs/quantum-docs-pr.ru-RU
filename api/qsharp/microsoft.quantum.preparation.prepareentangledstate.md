---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: Операция Препаринтангледстате
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 299d586f7581acdecf22da2f6bbfbb8d45f372f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732176"
---
# <a name="prepareentangledstate-operation"></a><span data-ttu-id="aac9a-102">Операция Препаринтангледстате</span><span class="sxs-lookup"><span data-stu-id="aac9a-102">PrepareEntangledState operation</span></span>

<span data-ttu-id="aac9a-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="aac9a-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="aac9a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aac9a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aac9a-105">Парные ентанглес два регистра кубит.</span><span class="sxs-lookup"><span data-stu-id="aac9a-105">Pairwise entangles two qubit registers.</span></span>

<span data-ttu-id="aac9a-106">Это значит, что при наличии двух регистров подготавливается максимальное запутанными State $ \фрак {1} {\скрт {2} } \лефт (\кет {00} + \кет {11} \ригхт) $ между каждой парой Кубитс в соответствующих регистрах, предполагая, что каждый регистр начинается в состоянии $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="aac9a-106">That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.</span></span>

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="aac9a-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="aac9a-107">Input</span></span>

### <a name="left--qubit"></a><span data-ttu-id="aac9a-108">Left: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="aac9a-108">left : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="aac9a-109">Массив кубит в состоянии $ \ket{0\cdots 0} $</span><span class="sxs-lookup"><span data-stu-id="aac9a-109">A qubit array in the $\ket{0\cdots 0}$ state</span></span>


### <a name="right--qubit"></a><span data-ttu-id="aac9a-110">Right: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="aac9a-110">right : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="aac9a-111">Массив кубит в состоянии $ \ket{0\cdots 0} $</span><span class="sxs-lookup"><span data-stu-id="aac9a-111">A qubit array in the $\ket{0\cdots 0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="aac9a-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aac9a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

