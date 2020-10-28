---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingFromBEandQubit
title: Операция Апплиблоккенкодингфромбеандкубит
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingFromBEandQubit
qsharp.summary: Conversion of ((LittleEndian, Qubit[]) => () is Adj + Ctl) to BlockEncoding
ms.openlocfilehash: d11c5bd8a33fc5dfc9ed3aa374c9c53afe286e24
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732136"
---
# <a name="applyblockencodingfrombeandqubit-operation"></a><span data-ttu-id="e556e-102">Операция Апплиблоккенкодингфромбеандкубит</span><span class="sxs-lookup"><span data-stu-id="e556e-102">ApplyBlockEncodingFromBEandQubit operation</span></span>

<span data-ttu-id="e556e-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e556e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e556e-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e556e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e556e-105">Преобразование ((Литтлиндиан, кубит []) => () является суммой и CTL) на Блоккенкодинг</span><span class="sxs-lookup"><span data-stu-id="e556e-105">Conversion of ((LittleEndian, Qubit[]) => () is Adj + Ctl) to BlockEncoding</span></span>

```qsharp
operation ApplyBlockEncodingFromBEandQubit (op : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl), auxiliary : Qubit[], system : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e556e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e556e-106">Input</span></span>

### <a name="op--littleendianqubit--unit-adj--ctl"></a><span data-ttu-id="e556e-107">Op: ([литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная начисление [единиц](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="e556e-107">op : ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="auxiliary--qubit"></a><span data-ttu-id="e556e-108">вспомогательная: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e556e-108">auxiliary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="system--qubit"></a><span data-ttu-id="e556e-109">System: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e556e-109">system : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="e556e-110">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e556e-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

