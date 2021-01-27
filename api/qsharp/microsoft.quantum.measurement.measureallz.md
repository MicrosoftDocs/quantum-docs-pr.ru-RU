---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Операция Меасуреаллз
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: cb3c7cab33efb612bbf5da3b51d2df5d1b8ba1df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854670"
---
# <a name="measureallz-operation"></a><span data-ttu-id="76168-102">Операция Меасуреаллз</span><span class="sxs-lookup"><span data-stu-id="76168-102">MeasureAllZ operation</span></span>

<span data-ttu-id="76168-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="76168-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="76168-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="76168-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="76168-105">Совместно измеряет регистр Кубитс на основе Паули Z.</span><span class="sxs-lookup"><span data-stu-id="76168-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="76168-106">Описание</span><span class="sxs-lookup"><span data-stu-id="76168-106">Description</span></span>

<span data-ttu-id="76168-107">Измеряет регистр Кубитс в $Z \отимес Z \отимес \кдотс \отимес Z $, представляющий четность всего регистра.</span><span class="sxs-lookup"><span data-stu-id="76168-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="76168-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="76168-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="76168-109">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="76168-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="76168-110">Регистр для измерения.</span><span class="sxs-lookup"><span data-stu-id="76168-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="76168-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="76168-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="76168-112">Результат измерения $Z \отимес Z \отимес \кдотс \отимес Z $.</span><span class="sxs-lookup"><span data-stu-id="76168-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>