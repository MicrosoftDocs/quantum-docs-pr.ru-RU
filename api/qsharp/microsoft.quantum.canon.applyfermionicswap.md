---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Операция Апплифермиониксвап
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 0c470705843a6360df0a72374570d86571397e41
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218807"
---
# <a name="applyfermionicswap-operation"></a><span data-ttu-id="8f6ff-102">Операция Апплифермиониксвап</span><span class="sxs-lookup"><span data-stu-id="8f6ff-102">ApplyFermionicSWAP operation</span></span>

<span data-ttu-id="8f6ff-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8f6ff-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8f6ff-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8f6ff-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8f6ff-105">Применяет ПЕРЕМЕНную Фермионик.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-105">Applies the Fermionic SWAP.</span></span>

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="8f6ff-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8f6ff-106">Description</span></span>

<span data-ttu-id="8f6ff-107">Это по сути меняет местами Кубитс при применении глобального этапа – 1, если оба Кубитс равны 1.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-107">This essentially swaps the qubits while applying a global phase of -1 if both qubits are 1s.</span></span> <span data-ttu-id="8f6ff-108">Сохраняет симметризатион орбиты.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-108">Preserves anti-symmetrization of orbitals.</span></span>
<span data-ttu-id="8f6ff-109">Дополнительные сведения см. в разделе .</span><span class="sxs-lookup"><span data-stu-id="8f6ff-109">See  for more information.</span></span>

<span data-ttu-id="8f6ff-110">Эта операция представлена единым оператором \бегин{алигн} f_ {swap} \масрел{: =} \бегин{бматрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-1 \\ \\ \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-110">This operation is represented by the unitary operator \begin{align} f_{swap} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -1 \\\\ \end{bmatrix}.</span></span>
<span data-ttu-id="8f6ff-111">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="8f6ff-111">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="8f6ff-112">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8f6ff-112">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="8f6ff-113">qubit1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8f6ff-113">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8f6ff-114">Первый кубит, который необходимо поменять местами.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-114">The first qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="8f6ff-115">qubit2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8f6ff-115">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8f6ff-116">Второй кубит, который необходимо поменять местами.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-116">The second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8f6ff-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8f6ff-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="8f6ff-118">Ссылки</span><span class="sxs-lookup"><span data-stu-id="8f6ff-118">References</span></span>

- [<span data-ttu-id="8f6ff-119">*Райан баббуш, (Nathan виебе, Жаррод Астрид, Джеймс мкклаин, Хартмут Невен, гарнет Kin-Lic* канал, арксив: 1706.00023</span><span class="sxs-lookup"><span data-stu-id="8f6ff-119"> *Ryan Babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic Chan*, arXiv:1706.00023 </span></span>](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a><span data-ttu-id="8f6ff-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="8f6ff-120">See Also</span></span>

- [<span data-ttu-id="8f6ff-121">Microsoft. тактов. внутренний. SWAP</span><span class="sxs-lookup"><span data-stu-id="8f6ff-121">Microsoft.Quantum.Intrinsic.SWAP</span></span>](xref:Microsoft.Quantum.Intrinsic.SWAP)