---
uid: Microsoft.Quantum.Characterization.ApplyHadamardTest
title: Операция Апплихадамардтест
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ApplyHadamardTest
qsharp.summary: ''
ms.openlocfilehash: 9918b520afdf2431067f568ee9994945ca52472a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216410"
---
# <a name="applyhadamardtest-operation"></a><span data-ttu-id="1b3ea-102">Операция Апплихадамардтест</span><span class="sxs-lookup"><span data-stu-id="1b3ea-102">ApplyHadamardTest operation</span></span>

<span data-ttu-id="1b3ea-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="1b3ea-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="1b3ea-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1b3ea-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyHadamardTest (phaseShift : Bool, commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), control : Qubit, target : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="1b3ea-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1b3ea-105">Input</span></span>

### <a name="phaseshift--bool"></a><span data-ttu-id="1b3ea-106">Фасешифт: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1b3ea-106">phaseShift : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="commonpreparation--qubit--unit--is-adj"></a><span data-ttu-id="1b3ea-107">Коммонпрепаратион: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) ></span><span class="sxs-lookup"><span data-stu-id="1b3ea-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="preparation1--qubit--unit--is-adj--ctl"></a><span data-ttu-id="1b3ea-108">preparation1: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="1b3ea-108">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="preparation2--qubit--unit--is-adj--ctl"></a><span data-ttu-id="1b3ea-109">preparation2: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="1b3ea-109">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="control--qubit"></a><span data-ttu-id="1b3ea-110">элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="1b3ea-110">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="target--qubit"></a><span data-ttu-id="1b3ea-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="1b3ea-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="1b3ea-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1b3ea-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

