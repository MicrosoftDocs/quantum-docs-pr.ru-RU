---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: Операция Препаринтангледстате
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 9bf42131860b9fe9bd223ade32f95ec747abefe8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854367"
---
# <a name="prepareentangledstate-operation"></a><span data-ttu-id="9b562-102">Операция Препаринтангледстате</span><span class="sxs-lookup"><span data-stu-id="9b562-102">PrepareEntangledState operation</span></span>

<span data-ttu-id="9b562-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="9b562-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="9b562-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9b562-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9b562-105">Парные ентанглес два регистра кубит.</span><span class="sxs-lookup"><span data-stu-id="9b562-105">Pairwise entangles two qubit registers.</span></span>

<span data-ttu-id="9b562-106">Это значит, что при наличии двух регистров подготавливается максимальное запутанными State $ \фрак {1} {\скрт {2} } \лефт (\кет {00} + \кет {11} \ригхт) $ между каждой парой Кубитс в соответствующих регистрах, предполагая, что каждый регистр начинается в состоянии $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="9b562-106">That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.</span></span>

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9b562-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9b562-107">Input</span></span>

### <a name="left--qubit"></a><span data-ttu-id="9b562-108">Left: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9b562-108">left : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9b562-109">Массив кубит в состоянии $ \ket{0\cdots 0} $</span><span class="sxs-lookup"><span data-stu-id="9b562-109">A qubit array in the $\ket{0\cdots 0}$ state</span></span>


### <a name="right--qubit"></a><span data-ttu-id="9b562-110">Right: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9b562-110">right : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9b562-111">Массив кубит в состоянии $ \ket{0\cdots 0} $</span><span class="sxs-lookup"><span data-stu-id="9b562-111">A qubit array in the $\ket{0\cdots 0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="9b562-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9b562-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

