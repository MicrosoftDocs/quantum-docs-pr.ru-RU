---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Определяемый пользователем тип Статеженератор
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: b4f6c3ca28e2976b6a0d58f4ef25ea943de9811e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854877"
---
# <a name="stategenerator-user-defined-type"></a><span data-ttu-id="a49a5-102">Определяемый пользователем тип Статеженератор</span><span class="sxs-lookup"><span data-stu-id="a49a5-102">StateGenerator user defined type</span></span>

<span data-ttu-id="a49a5-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a49a5-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="a49a5-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a49a5-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="a49a5-105">Описывает операцию, которая подготавливает заданный вход для последовательного классификатора.</span><span class="sxs-lookup"><span data-stu-id="a49a5-105">Describes an operation that prepares a given input to a sequential classifier.</span></span>

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="a49a5-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="a49a5-106">Named Items</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="a49a5-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a49a5-107">NQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a49a5-108">Число Кубитс, для которых определено закодированное входное значение.</span><span class="sxs-lookup"><span data-stu-id="a49a5-108">The number of qubits on which the encoded input is defined.</span></span>
### <a name="prepare--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="a49a5-109">Подготовка: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="a49a5-109">Prepare : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a49a5-110">Операция, которая подготавливает закодированные входные данные к регистру Кубитс с прямым порядком следования `NQubits` .</span><span class="sxs-lookup"><span data-stu-id="a49a5-110">An operation which prepares the encoded input on a little-endian register of `NQubits` qubits.</span></span>