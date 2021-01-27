---
uid: Microsoft.Quantum.Chemistry.JordanWigner.SelectZ
title: Операция Селектз
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: SelectZ
qsharp.summary: A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$. That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$
ms.openlocfilehash: 2b38be5c196d81635daa8b478f6e727fdf378c62
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850239"
---
# <a name="selectz-operation"></a><span data-ttu-id="5cd98-102">Операция Селектз</span><span class="sxs-lookup"><span data-stu-id="5cd98-102">SelectZ operation</span></span>

<span data-ttu-id="5cd98-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="5cd98-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="5cd98-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="5cd98-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="5cd98-105">Единая $U $, которая применяет шлюз Паули $Z $ к Кубитс $p $ с состоянием индекса $ \кет{п} $.</span><span class="sxs-lookup"><span data-stu-id="5cd98-105">A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$.</span></span> <span data-ttu-id="5cd98-106">Т. е. $ $ \бегин{алигн} У\кет {p} \ Сисакет {\ PSI} = \Кет{п}з \_ п\кет {\ PSI} \енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="5cd98-106">That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$</span></span>

```qsharp
operation SelectZ (indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5cd98-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5cd98-107">Input</span></span>

### <a name="indexregister--littleendian"></a><span data-ttu-id="5cd98-108">Индексрегистер: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5cd98-108">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5cd98-109">Состояние $ \кет{п} $ этого регистра определяет кубит, к которому применяется $Z $.</span><span class="sxs-lookup"><span data-stu-id="5cd98-109">The state $\ket{p}$ of this register determines the qubit on which $Z$ is applied.</span></span>


### <a name="targetregister--qubit"></a><span data-ttu-id="5cd98-110">Таржетрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5cd98-110">targetRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5cd98-111">Регистрация Кубитс, к которой применяются операторы Паули.</span><span class="sxs-lookup"><span data-stu-id="5cd98-111">Register of qubits on which the Pauli operators are applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5cd98-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5cd98-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

