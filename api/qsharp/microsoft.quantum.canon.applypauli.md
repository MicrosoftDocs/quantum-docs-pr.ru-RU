---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: Операция Апплипаули
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: ccf8e1b3dbe5d4cd916a581aeab190ab0cff2021
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717819"
---
# <a name="applypauli-operation"></a><span data-ttu-id="66a0f-102">Операция Апплипаули</span><span class="sxs-lookup"><span data-stu-id="66a0f-102">ApplyPauli operation</span></span>

<span data-ttu-id="66a0f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="66a0f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="66a0f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="66a0f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="66a0f-105">При наличии кубит оператора Паули применяет соответствующую операцию к регистру.</span><span class="sxs-lookup"><span data-stu-id="66a0f-105">Given a multi-qubit Pauli operator, applies the corresponding operation to a register.</span></span>

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="66a0f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="66a0f-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="66a0f-107">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="66a0f-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="66a0f-108">Оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули.</span><span class="sxs-lookup"><span data-stu-id="66a0f-108">A multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="66a0f-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="66a0f-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="66a0f-110">Зарегистрируйтесь, чтобы применить данную операцию Паули к.</span><span class="sxs-lookup"><span data-stu-id="66a0f-110">Register to apply the given Pauli operation on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="66a0f-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="66a0f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
