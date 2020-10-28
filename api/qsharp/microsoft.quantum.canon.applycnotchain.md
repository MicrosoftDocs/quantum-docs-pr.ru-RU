---
uid: Microsoft.Quantum.Canon.ApplyCNOTChain
title: Операция Аппликнотчаин
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChain
qsharp.summary: Computes the parity of a register of qubits in-place.
ms.openlocfilehash: c98fe24ca352952162acb7a9c4fc93d5da4285b8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729688"
---
# <a name="applycnotchain-operation"></a><span data-ttu-id="07768-102">Операция Аппликнотчаин</span><span class="sxs-lookup"><span data-stu-id="07768-102">ApplyCNOTChain operation</span></span>

<span data-ttu-id="07768-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="07768-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="07768-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="07768-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="07768-105">Вычисление четности регистра Кубитс на месте.</span><span class="sxs-lookup"><span data-stu-id="07768-105">Computes the parity of a register of qubits in-place.</span></span>

```qsharp
operation ApplyCNOTChain (qubits : Qubit[]) : Unit
```


## <a name="description"></a><span data-ttu-id="07768-106">Описание</span><span class="sxs-lookup"><span data-stu-id="07768-106">Description</span></span>

<span data-ttu-id="07768-107">Эта операция преобразует состояние входа как $ $ \бегин{алигн} \кет{q_0} \кет{q_1} \кдотс \кет{q_ {n-1}} & \мапсто \кет{q_0} \кет{q_0 \оплус q_1} \кет{q_0 \оплус q_1 \оплус q_2} \кдотс \ket{q_0 \oplus \cdots \oplus q_ {n-1}}.</span><span class="sxs-lookup"><span data-stu-id="07768-107">This operation transforms the state of its input as $$ \begin{align} \ket{q_0} \ket{q_1} \cdots \ket{q_{n - 1}} & \mapsto \ket{q_0} \ket{q_0 \oplus q_1} \ket{q_0 \oplus q_1 \oplus q_2} \cdots \ket{q_0 \oplus \cdots \oplus q_{n - 1}}.</span></span>
<span data-ttu-id="07768-108">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="07768-108">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="07768-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="07768-109">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="07768-110">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="07768-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="07768-111">Массив Кубитс, для которого необходимо вычислить и сохранить контрольные суммы.</span><span class="sxs-lookup"><span data-stu-id="07768-111">Array of qubits whose parity is to be computed and stored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="07768-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="07768-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

