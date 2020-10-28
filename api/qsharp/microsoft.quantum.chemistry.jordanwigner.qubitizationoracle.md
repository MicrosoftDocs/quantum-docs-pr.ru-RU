---
uid: Microsoft.Quantum.Chemistry.JordanWigner.QubitizationOracle
title: Функция Кубитизатионоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: QubitizationOracle
qsharp.summary: Returns Qubitization operation and the parameters necessary to run it.
ms.openlocfilehash: 326bebfc1cfd839082732898167c20ecf105a266
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713815"
---
# <a name="qubitizationoracle-function"></a><span data-ttu-id="b3df9-102">Функция Кубитизатионоракле</span><span class="sxs-lookup"><span data-stu-id="b3df9-102">QubitizationOracle function</span></span>

<span data-ttu-id="b3df9-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="b3df9-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="b3df9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b3df9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b3df9-105">Возвращает операцию Кубитизатион и параметры, необходимые для ее запуска.</span><span class="sxs-lookup"><span data-stu-id="b3df9-105">Returns Qubitization operation and the parameters necessary to run it.</span></span>

```qsharp
function QubitizationOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a><span data-ttu-id="b3df9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b3df9-106">Input</span></span>

### <a name="qsharpdata--jordanwignerencodingdata"></a><span data-ttu-id="b3df9-107">Кшарпдата: [жорданвигнеренкодингдата](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="b3df9-107">qSharpData : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="b3df9-108">Хамилтониан, описанный в разделе `JordanWignerEncodingData` format.</span><span class="sxs-lookup"><span data-stu-id="b3df9-108">Hamiltonian described by `JordanWignerEncodingData` format.</span></span>



## <a name="output--intdoublequbit--unit-adj--ctl"></a><span data-ttu-id="b3df9-109">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL))</span><span class="sxs-lookup"><span data-stu-id="b3df9-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl))</span></span>

<span data-ttu-id="b3df9-110">Кортеж, где: `Int` — число Кубитс, `Double` — это одноразовая норма хамилтониан коэффициентов, а операция — это проход такта, созданный кубитизатион.</span><span class="sxs-lookup"><span data-stu-id="b3df9-110">A tuple where: `Int` is the number of qubits allocated, `Double` is the one-norm of Hamiltonian coefficients, and the operation is the Quantum walk created by Qubitization.</span></span>