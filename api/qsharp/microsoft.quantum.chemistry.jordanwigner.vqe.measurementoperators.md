---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Функция Меасурементоператорс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 204ae621b77559a894f0bce14e494824d58e4ad6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835400"
---
# <a name="measurementoperators-function"></a><span data-ttu-id="fd3db-102">Функция Меасурементоператорс</span><span class="sxs-lookup"><span data-stu-id="fd3db-102">MeasurementOperators function</span></span>

<span data-ttu-id="fd3db-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="fd3db-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="fd3db-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="fd3db-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="fd3db-105">Вычисление всех операторов измерения, необходимых для расчета ожидания Jordan-Wigner термина.</span><span class="sxs-lookup"><span data-stu-id="fd3db-105">Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.</span></span>

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="fd3db-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fd3db-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="fd3db-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fd3db-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fd3db-108">Число Кубитс, необходимое для имитации системы молекулярное.</span><span class="sxs-lookup"><span data-stu-id="fd3db-108">The number of qubits required to simulate the molecular system.</span></span>


### <a name="indices--int"></a><span data-ttu-id="fd3db-109">индексы: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="fd3db-109">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="fd3db-110">Массив, содержащий индексы кубит, к которым применяется каждый оператор Паули.</span><span class="sxs-lookup"><span data-stu-id="fd3db-110">An array containing the indices of the qubit each Pauli operator is applied to.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="fd3db-111">Термтипе: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fd3db-111">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fd3db-112">Тип Jordan-Wigner термина.</span><span class="sxs-lookup"><span data-stu-id="fd3db-112">The type of the Jordan-Wigner term.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="fd3db-113">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="fd3db-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="fd3db-114">Массив операторов измерения (каждый из которых является массивом из Паули).</span><span class="sxs-lookup"><span data-stu-id="fd3db-114">An array of measurement operators (each being an array of Pauli).</span></span>