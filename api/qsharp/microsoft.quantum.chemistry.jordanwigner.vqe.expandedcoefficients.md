---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: Функция ЕкспандедкоеффиЦиентс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: b953fb8f5737956e8597cd90a7d6bfc0bafce4e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835619"
---
# <a name="expandedcoefficients-function"></a><span data-ttu-id="20d4a-102">Функция ЕкспандедкоеффиЦиентс</span><span class="sxs-lookup"><span data-stu-id="20d4a-102">ExpandedCoefficients function</span></span>

<span data-ttu-id="20d4a-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="20d4a-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="20d4a-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="20d4a-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="20d4a-105">Развертывает компактное представление Jordan-Wigner коэффициенты для получения однозначного сопоставления между этими и Паули терминами.</span><span class="sxs-lookup"><span data-stu-id="20d4a-105">Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.</span></span>

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="20d4a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="20d4a-106">Input</span></span>

### <a name="coeff--double"></a><span data-ttu-id="20d4a-107">коефф: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="20d4a-107">coeff : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="20d4a-108">Массив коэффициентов, считываемых из структуры данных Jordan-Wigner Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="20d4a-108">An array of coefficients, as read from the Jordan-Wigner Hamiltonian data structure.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="20d4a-109">Термтипе: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="20d4a-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="20d4a-110">Тип Jordan-Wigner термина.</span><span class="sxs-lookup"><span data-stu-id="20d4a-110">The type of the Jordan-Wigner term.</span></span>



## <a name="output--double"></a><span data-ttu-id="20d4a-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="20d4a-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="20d4a-112">Расширенные массивы коэффициентов, по одному на каждый Паули термин.</span><span class="sxs-lookup"><span data-stu-id="20d4a-112">Expanded arrays of coefficients, one per Pauli term.</span></span>