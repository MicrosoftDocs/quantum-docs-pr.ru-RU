---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Операция Меасуреаллз
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 6c44ab6a7983697644071f0e3cf106e9825661ee
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227086"
---
# <a name="measureallz-operation"></a><span data-ttu-id="f0b11-102">Операция Меасуреаллз</span><span class="sxs-lookup"><span data-stu-id="f0b11-102">MeasureAllZ operation</span></span>

<span data-ttu-id="f0b11-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="f0b11-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="f0b11-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f0b11-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f0b11-105">Совместно измеряет регистр Кубитс на основе Паули Z.</span><span class="sxs-lookup"><span data-stu-id="f0b11-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="f0b11-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f0b11-106">Description</span></span>

<span data-ttu-id="f0b11-107">Измеряет регистр Кубитс в $Z \отимес Z \отимес \кдотс \отимес Z $, представляющий четность всего регистра.</span><span class="sxs-lookup"><span data-stu-id="f0b11-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="f0b11-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f0b11-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="f0b11-109">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f0b11-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f0b11-110">Регистр для измерения.</span><span class="sxs-lookup"><span data-stu-id="f0b11-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="f0b11-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="f0b11-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="f0b11-112">Результат измерения $Z \отимес Z \отимес \кдотс \отимес Z $.</span><span class="sxs-lookup"><span data-stu-id="f0b11-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>