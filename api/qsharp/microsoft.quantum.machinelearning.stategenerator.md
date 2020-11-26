---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Определяемый пользователем тип Статеженератор
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: 5c9643f5c917ff3cb25fa8c046856b03cc287edd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211565"
---
# <a name="stategenerator-user-defined-type"></a><span data-ttu-id="4dac2-102">Определяемый пользователем тип Статеженератор</span><span class="sxs-lookup"><span data-stu-id="4dac2-102">StateGenerator user defined type</span></span>

<span data-ttu-id="4dac2-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="4dac2-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="4dac2-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="4dac2-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="4dac2-105">Описывает операцию, которая подготавливает заданный вход для последовательного классификатора.</span><span class="sxs-lookup"><span data-stu-id="4dac2-105">Describes an operation that prepares a given input to a sequential classifier.</span></span>

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="4dac2-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="4dac2-106">Named Items</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="4dac2-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4dac2-107">NQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4dac2-108">Число Кубитс, для которых определено закодированное входное значение.</span><span class="sxs-lookup"><span data-stu-id="4dac2-108">The number of qubits on which the encoded input is defined.</span></span>
### <a name="prepare--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="4dac2-109">Подготовка: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="4dac2-109">Prepare : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="4dac2-110">Операция, которая подготавливает закодированные входные данные к регистру Кубитс с прямым порядком следования `NQubits` .</span><span class="sxs-lookup"><span data-stu-id="4dac2-110">An operation which prepares the encoded input on a little-endian register of `NQubits` qubits.</span></span>