---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Функция Фассадамардтрансформед
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: 3e48701f22ddf154721355866e15a85fca0bc7df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203099"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="dfba2-102">Функция Фассадамардтрансформед</span><span class="sxs-lookup"><span data-stu-id="dfba2-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="dfba2-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="dfba2-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="dfba2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dfba2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dfba2-105">Вычисление Хадамард преобразования логической функции в {-1,1} кодировке с помощью метода Йейтса</span><span class="sxs-lookup"><span data-stu-id="dfba2-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="dfba2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="dfba2-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="dfba2-107">Func: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="dfba2-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="dfba2-108">Истинная таблица в {-1,1} кодировке</span><span class="sxs-lookup"><span data-stu-id="dfba2-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="dfba2-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="dfba2-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="dfba2-110">Спектрал коэффициенты функции</span><span class="sxs-lookup"><span data-stu-id="dfba2-110">Spectral coefficients of the function</span></span>