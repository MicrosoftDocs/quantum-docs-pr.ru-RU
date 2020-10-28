---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Операция Меасуреаллз
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 4ac36a77b37f672859e61f3db89a43f4ca1fc93c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711072"
---
# <a name="measureallz-operation"></a><span data-ttu-id="16132-102">Операция Меасуреаллз</span><span class="sxs-lookup"><span data-stu-id="16132-102">MeasureAllZ operation</span></span>

<span data-ttu-id="16132-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="16132-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="16132-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="16132-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="16132-105">Совместно измеряет регистр Кубитс на основе Паули Z.</span><span class="sxs-lookup"><span data-stu-id="16132-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="16132-106">Описание</span><span class="sxs-lookup"><span data-stu-id="16132-106">Description</span></span>

<span data-ttu-id="16132-107">Измеряет регистр Кубитс в $Z \отимес Z \отимес \кдотс \отимес Z $, представляющий четность всего регистра.</span><span class="sxs-lookup"><span data-stu-id="16132-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="16132-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="16132-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="16132-109">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="16132-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="16132-110">Регистр для измерения.</span><span class="sxs-lookup"><span data-stu-id="16132-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="16132-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="16132-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="16132-112">Результат измерения $Z \отимес Z \отимес \кдотс \отимес Z $.</span><span class="sxs-lookup"><span data-stu-id="16132-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>