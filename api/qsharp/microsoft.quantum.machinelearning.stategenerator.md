---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Определяемый пользователем тип Статеженератор
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: e3026dbae7209acd41924c0038a6f9b2c4b41197
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732304"
---
# <a name="stategenerator-user-defined-type"></a><span data-ttu-id="8aa39-102">Определяемый пользователем тип Статеженератор</span><span class="sxs-lookup"><span data-stu-id="8aa39-102">StateGenerator user defined type</span></span>

<span data-ttu-id="8aa39-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8aa39-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="8aa39-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8aa39-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8aa39-105">Описывает операцию, которая подготавливает заданный вход для последовательного классификатора.</span><span class="sxs-lookup"><span data-stu-id="8aa39-105">Describes an operation that prepares a given input to a sequential classifier.</span></span>

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="8aa39-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="8aa39-106">Named Items</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="8aa39-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8aa39-107">NQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8aa39-108">Число Кубитс, для которых определено закодированное входное значение.</span><span class="sxs-lookup"><span data-stu-id="8aa39-108">The number of qubits on which the encoded input is defined.</span></span>
### <a name="prepare--littleendian--unit-adj--ctl"></a><span data-ttu-id="8aa39-109">Подготовка: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="8aa39-109">Prepare : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="8aa39-110">Операция, которая подготавливает закодированные входные данные к регистру Кубитс с прямым порядком следования `NQubits` .</span><span class="sxs-lookup"><span data-stu-id="8aa39-110">An operation which prepares the encoded input on a little-endian register of `NQubits` qubits.</span></span>