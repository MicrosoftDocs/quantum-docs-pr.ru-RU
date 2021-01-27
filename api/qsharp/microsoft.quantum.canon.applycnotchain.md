---
uid: Microsoft.Quantum.Canon.ApplyCNOTChain
title: Операция Аппликнотчаин
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChain
qsharp.summary: Computes the parity of a register of qubits in-place.
ms.openlocfilehash: b5a74eb66529095233c89a4ec7ea37c996458cb4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841964"
---
# <a name="applycnotchain-operation"></a><span data-ttu-id="a0f16-102">Операция Аппликнотчаин</span><span class="sxs-lookup"><span data-stu-id="a0f16-102">ApplyCNOTChain operation</span></span>

<span data-ttu-id="a0f16-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a0f16-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a0f16-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a0f16-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a0f16-105">Вычисление четности регистра Кубитс на месте.</span><span class="sxs-lookup"><span data-stu-id="a0f16-105">Computes the parity of a register of qubits in-place.</span></span>

```qsharp
operation ApplyCNOTChain (qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a0f16-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a0f16-106">Description</span></span>

<span data-ttu-id="a0f16-107">Эта операция преобразует состояние входа как $ $ \бегин{алигн} \кет{q_0} \кет{q_1} \кдотс \кет{q_ {n-1}} & \мапсто \кет{q_0} \кет{q_0 \оплус q_1} \кет{q_0 \оплус q_1 \оплус q_2} \кдотс \ket{q_0 \oplus \cdots \oplus q_ {n-1}}.</span><span class="sxs-lookup"><span data-stu-id="a0f16-107">This operation transforms the state of its input as $$ \begin{align} \ket{q_0} \ket{q_1} \cdots \ket{q_{n - 1}} & \mapsto \ket{q_0} \ket{q_0 \oplus q_1} \ket{q_0 \oplus q_1 \oplus q_2} \cdots \ket{q_0 \oplus \cdots \oplus q_{n - 1}}.</span></span>
<span data-ttu-id="a0f16-108">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="a0f16-108">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="a0f16-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a0f16-109">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="a0f16-110">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a0f16-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a0f16-111">Массив Кубитс, для которого необходимо вычислить и сохранить контрольные суммы.</span><span class="sxs-lookup"><span data-stu-id="a0f16-111">Array of qubits whose parity is to be computed and stored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a0f16-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a0f16-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

