---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: Операция Апплипаулифромбитстринг
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: 09754accb92c1339b781003e5722e3c8f5884e6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717806"
---
# <a name="applypaulifrombitstring-operation"></a><span data-ttu-id="e89a9-102">Операция Апплипаулифромбитстринг</span><span class="sxs-lookup"><span data-stu-id="e89a9-102">ApplyPauliFromBitString operation</span></span>

<span data-ttu-id="e89a9-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e89a9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e89a9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e89a9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e89a9-105">Применяет оператор Паули к каждому кубит в массиве, если соответствующий бит логического массива совпадает с заданным входным значением.</span><span class="sxs-lookup"><span data-stu-id="e89a9-105">Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.</span></span>

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e89a9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e89a9-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="e89a9-107">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="e89a9-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="e89a9-108">Оператор Паули для применения к `qubits[idx]` месту `bitsApply == bits[idx]`</span><span class="sxs-lookup"><span data-stu-id="e89a9-108">Pauli operator to apply to `qubits[idx]` where `bitsApply == bits[idx]`</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="e89a9-109">Битаппли: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e89a9-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e89a9-110">применить Паули, если бит — это значение</span><span class="sxs-lookup"><span data-stu-id="e89a9-110">apply Pauli if bit is this value</span></span>


### <a name="bits--bool"></a><span data-ttu-id="e89a9-111">Разрядность: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="e89a9-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="e89a9-112">Логический регистр, указывающий, на какие соответствующие кубит `qubits` должны работать</span><span class="sxs-lookup"><span data-stu-id="e89a9-112">Boolean register specifying which corresponding qubit in `qubits` should be operated on</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="e89a9-113">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e89a9-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e89a9-114">Регистр такта, на котором выборочно применяется указанный оператор Паули</span><span class="sxs-lookup"><span data-stu-id="e89a9-114">Quantum register on which to selectively apply the specified Pauli operator</span></span>



## <a name="output--unit"></a><span data-ttu-id="e89a9-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e89a9-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e89a9-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="e89a9-116">Remarks</span></span>

<span data-ttu-id="e89a9-117">Логический массив и регистр такта должны иметь одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="e89a9-117">The Boolean array and the quantum register must be of equal length.</span></span>