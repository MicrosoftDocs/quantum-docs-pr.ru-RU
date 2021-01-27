---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: Операция Апплипаули
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: b3557c6d8b5a90019f6d4cfa7b405475a3ab39fb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844743"
---
# <a name="applypauli-operation"></a><span data-ttu-id="91e41-102">Операция Апплипаули</span><span class="sxs-lookup"><span data-stu-id="91e41-102">ApplyPauli operation</span></span>

<span data-ttu-id="91e41-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="91e41-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="91e41-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="91e41-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="91e41-105">При наличии кубит оператора Паули применяет соответствующую операцию к регистру.</span><span class="sxs-lookup"><span data-stu-id="91e41-105">Given a multi-qubit Pauli operator, applies the corresponding operation to a register.</span></span>

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="91e41-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="91e41-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="91e41-107">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="91e41-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="91e41-108">Оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули.</span><span class="sxs-lookup"><span data-stu-id="91e41-108">A multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="91e41-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="91e41-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="91e41-110">Зарегистрируйтесь, чтобы применить данную операцию Паули к.</span><span class="sxs-lookup"><span data-stu-id="91e41-110">Register to apply the given Pauli operation on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="91e41-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="91e41-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="91e41-112">Пример</span><span class="sxs-lookup"><span data-stu-id="91e41-112">Example</span></span>

<span data-ttu-id="91e41-113">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="91e41-113">The following are equivalent:</span></span>

```qsharp
ApplyPauli([PauliY, PauliZ, PauliX], target);
```

<span data-ttu-id="91e41-114">и</span><span class="sxs-lookup"><span data-stu-id="91e41-114">and</span></span>

```qsharp
Y(target[0]);
Z(target[1]);
X(target[2]);
```