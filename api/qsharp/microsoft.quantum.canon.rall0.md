---
uid: Microsoft.Quantum.Canon.RAll0
title: Операция RAll0
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll0
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.
ms.openlocfilehash: bd1f796209a15f290315e55b872ae3b3e508a68b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205666"
---
# <a name="rall0-operation"></a><span data-ttu-id="5c1ec-102">Операция RAll0</span><span class="sxs-lookup"><span data-stu-id="5c1ec-102">RAll0 operation</span></span>

<span data-ttu-id="5c1ec-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5c1ec-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5c1ec-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5c1ec-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5c1ec-105">Выполняет операцию сдвига этапа.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-105">Performs a phase shift operation.</span></span>

<span data-ttu-id="5c1ec-106">$R = \болдоне-(1-e ^ {i \фи}) \ket{0\cdots 0} \bra{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-106">$R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.</span></span>

```qsharp
operation RAll0 (phase : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5c1ec-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5c1ec-107">Input</span></span>

### <a name="phase--double"></a><span data-ttu-id="5c1ec-108">этап: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5c1ec-108">phase : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5c1ec-109">Этап $ \фи $ применен к состоянию $ \ket{0\cdots 0} \bra{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-109">The phase $\phi$ applied to state $\ket{0\cdots 0}\bra{0\cdots 0}$.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="5c1ec-110">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5c1ec-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5c1ec-111">Регистр, состояние которого необходимо поворачивать $R $.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-111">The register whose state is to be rotated by $R$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5c1ec-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5c1ec-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="5c1ec-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="5c1ec-113">See Also</span></span>

- [<span data-ttu-id="5c1ec-114">Microsoft. тактов. Canon. RAll1</span><span class="sxs-lookup"><span data-stu-id="5c1ec-114">Microsoft.Quantum.Canon.RAll1</span></span>](xref:Microsoft.Quantum.Canon.RAll1)