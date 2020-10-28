---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Функция Меасурементоператорс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 24d752c4f198764b6e7c6ea6c49669c020c1a502
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713676"
---
# <a name="measurementoperators-function"></a><span data-ttu-id="836a8-102">Функция Меасурементоператорс</span><span class="sxs-lookup"><span data-stu-id="836a8-102">MeasurementOperators function</span></span>

<span data-ttu-id="836a8-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="836a8-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="836a8-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="836a8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="836a8-105">Вычисление всех операторов измерения, необходимых для расчета ожидания Jordan-Wigner термина.</span><span class="sxs-lookup"><span data-stu-id="836a8-105">Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.</span></span>

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="836a8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="836a8-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="836a8-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="836a8-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="836a8-108">Число Кубитс, необходимое для имитации системы молекулярное.</span><span class="sxs-lookup"><span data-stu-id="836a8-108">The number of qubits required to simulate the molecular system.</span></span>


### <a name="indices--int"></a><span data-ttu-id="836a8-109">индексы: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="836a8-109">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="836a8-110">Массив, содержащий индексы кубит, к которым применяется каждый оператор Паули.</span><span class="sxs-lookup"><span data-stu-id="836a8-110">An array containing the indices of the qubit each Pauli operator is applied to.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="836a8-111">Термтипе: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="836a8-111">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="836a8-112">Тип Jordan-Wigner термина.</span><span class="sxs-lookup"><span data-stu-id="836a8-112">The type of the Jordan-Wigner term.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="836a8-113">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="836a8-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="836a8-114">Массив операторов измерения (каждый из которых является массивом из Паули).</span><span class="sxs-lookup"><span data-stu-id="836a8-114">An array of measurement operators (each being an array of Pauli).</span></span>