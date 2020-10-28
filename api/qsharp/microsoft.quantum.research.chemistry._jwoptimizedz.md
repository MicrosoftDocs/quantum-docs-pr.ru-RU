---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedZ
title: _JWOptimizedZ операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedZ
qsharp.summary: Applies a Rz rotation, with a C-NOT trick to double phase in phase estimation.
ms.openlocfilehash: 8bbd4af0389a7b748be11dc50bacd2c178521adc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733577"
---
# <a name="_jwoptimizedz-operation"></a><span data-ttu-id="8643a-102">_JWOptimizedZ операция</span><span class="sxs-lookup"><span data-stu-id="8643a-102">_JWOptimizedZ operation</span></span>

<span data-ttu-id="8643a-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="8643a-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="8643a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8643a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8643a-105">Применяет поворот РЗ с нехитростью к удвоенному этапу в оценке фазы.</span><span class="sxs-lookup"><span data-stu-id="8643a-105">Applies a Rz rotation, with a C-NOT trick to double phase in phase estimation.</span></span>

```qsharp
operation _JWOptimizedZ (angle : Double, parityQubit : Qubit, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="8643a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8643a-106">Input</span></span>

### <a name="angle--double"></a><span data-ttu-id="8643a-107">угол: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8643a-107">angle : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8643a-108">Угол поворота РЗ.</span><span class="sxs-lookup"><span data-stu-id="8643a-108">Angle of Rz rotation.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="8643a-109">Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8643a-109">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8643a-110">Кубит, определяющий знак времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="8643a-110">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="8643a-111">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8643a-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="8643a-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8643a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

