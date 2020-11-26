---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: Операция Апплипаули
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: 7f42d9cab2f80f8f826ad1268b050134f0540cdd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218229"
---
# <a name="applypauli-operation"></a><span data-ttu-id="cda1d-102">Операция Апплипаули</span><span class="sxs-lookup"><span data-stu-id="cda1d-102">ApplyPauli operation</span></span>

<span data-ttu-id="cda1d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cda1d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cda1d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cda1d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cda1d-105">При наличии кубит оператора Паули применяет соответствующую операцию к регистру.</span><span class="sxs-lookup"><span data-stu-id="cda1d-105">Given a multi-qubit Pauli operator, applies the corresponding operation to a register.</span></span>

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="cda1d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cda1d-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="cda1d-107">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="cda1d-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="cda1d-108">Оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули.</span><span class="sxs-lookup"><span data-stu-id="cda1d-108">A multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="cda1d-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cda1d-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="cda1d-110">Зарегистрируйтесь, чтобы применить данную операцию Паули к.</span><span class="sxs-lookup"><span data-stu-id="cda1d-110">Register to apply the given Pauli operation on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cda1d-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cda1d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

