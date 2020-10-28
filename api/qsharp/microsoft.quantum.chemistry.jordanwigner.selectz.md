---
uid: Microsoft.Quantum.Chemistry.JordanWigner.SelectZ
title: Операция Селектз
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: SelectZ
qsharp.summary: A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$. That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$
ms.openlocfilehash: 171bbe28ce8f10ca4b213a94b23f8c049546e3bf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713788"
---
# <a name="selectz-operation"></a><span data-ttu-id="a99ed-102">Операция Селектз</span><span class="sxs-lookup"><span data-stu-id="a99ed-102">SelectZ operation</span></span>

<span data-ttu-id="a99ed-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="a99ed-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="a99ed-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a99ed-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a99ed-105">Единая $U $, которая применяет шлюз Паули $Z $ к Кубитс $p $ с состоянием индекса $ \кет{п} $.</span><span class="sxs-lookup"><span data-stu-id="a99ed-105">A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$.</span></span> <span data-ttu-id="a99ed-106">Т. е. $ $ \бегин{алигн} У\кет {p} \ Сисакет {\ PSI} = \Кет{п}з \_ п\кет {\ PSI} \енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="a99ed-106">That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$</span></span>

```qsharp
operation SelectZ (indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="a99ed-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a99ed-107">Input</span></span>

### <a name="indexregister--littleendian"></a><span data-ttu-id="a99ed-108">Индексрегистер: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a99ed-108">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a99ed-109">Состояние $ \кет{п} $ этого регистра определяет кубит, к которому применяется $Z $.</span><span class="sxs-lookup"><span data-stu-id="a99ed-109">The state $\ket{p}$ of this register determines the qubit on which $Z$ is applied.</span></span>


### <a name="targetregister--qubit"></a><span data-ttu-id="a99ed-110">Таржетрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a99ed-110">targetRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a99ed-111">Регистрация Кубитс, к которой применяются операторы Паули.</span><span class="sxs-lookup"><span data-stu-id="a99ed-111">Register of qubits on which the Pauli operators are applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a99ed-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a99ed-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

