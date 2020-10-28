---
uid: Microsoft.Quantum.Canon.RAll0
title: Операция RAll0
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll0
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.
ms.openlocfilehash: 6185e66e08d2af3aa0b35791638820b4dcc5af35
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715635"
---
# <a name="rall0-operation"></a><span data-ttu-id="bb031-102">Операция RAll0</span><span class="sxs-lookup"><span data-stu-id="bb031-102">RAll0 operation</span></span>

<span data-ttu-id="bb031-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bb031-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bb031-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bb031-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bb031-105">Выполняет операцию сдвига этапа.</span><span class="sxs-lookup"><span data-stu-id="bb031-105">Performs a phase shift operation.</span></span>

<span data-ttu-id="bb031-106">$R = \болдоне-(1-e ^ {i \фи}) \ket{0\cdots 0} \bra{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="bb031-106">$R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.</span></span>

```qsharp
operation RAll0 (phase : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="bb031-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bb031-107">Input</span></span>

### <a name="phase--double"></a><span data-ttu-id="bb031-108">этап: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bb031-108">phase : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bb031-109">Этап $ \фи $ применен к состоянию $ \ket{0\cdots 0} \bra{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="bb031-109">The phase $\phi$ applied to state $\ket{0\cdots 0}\bra{0\cdots 0}$.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="bb031-110">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bb031-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bb031-111">Регистр, состояние которого необходимо поворачивать $R $.</span><span class="sxs-lookup"><span data-stu-id="bb031-111">The register whose state is to be rotated by $R$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bb031-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bb031-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="bb031-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="bb031-113">See Also</span></span>

- [<span data-ttu-id="bb031-114">Microsoft. тактов. Canon. RAll1</span><span class="sxs-lookup"><span data-stu-id="bb031-114">Microsoft.Quantum.Canon.RAll1</span></span>](xref:Microsoft.Quantum.Canon.RAll1)