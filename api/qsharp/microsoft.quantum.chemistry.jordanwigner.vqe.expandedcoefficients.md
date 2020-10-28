---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: Функция ЕкспандедкоеффиЦиентс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: 8f5a2319b5839d0d9e47972389330dc16dffcaf0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713717"
---
# <a name="expandedcoefficients-function"></a><span data-ttu-id="0d1c4-102">Функция ЕкспандедкоеффиЦиентс</span><span class="sxs-lookup"><span data-stu-id="0d1c4-102">ExpandedCoefficients function</span></span>

<span data-ttu-id="0d1c4-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="0d1c4-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="0d1c4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0d1c4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0d1c4-105">Развертывает компактное представление Jordan-Wigner коэффициенты для получения однозначного сопоставления между этими и Паули терминами.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-105">Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.</span></span>

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="0d1c4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0d1c4-106">Input</span></span>

### <a name="coeff--double"></a><span data-ttu-id="0d1c4-107">коефф: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="0d1c4-107">coeff : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="0d1c4-108">Массив коэффициентов, считываемых из структуры данных Jordan-Wigner Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-108">An array of coefficients, as read from the Jordan-Wigner Hamiltonian data structure.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="0d1c4-109">Термтипе: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0d1c4-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0d1c4-110">Тип Jordan-Wigner термина.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-110">The type of the Jordan-Wigner term.</span></span>



## <a name="output--double"></a><span data-ttu-id="0d1c4-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="0d1c4-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="0d1c4-112">Расширенные массивы коэффициентов, по одному на каждый Паули термин.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-112">Expanded arrays of coefficients, one per Pauli term.</span></span>