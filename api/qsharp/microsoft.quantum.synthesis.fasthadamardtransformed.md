---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Функция Фассадамардтрансформед
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: 2b84e92d08a3baad2552780cae91f447830cac82
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733896"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="28003-102">Функция Фассадамардтрансформед</span><span class="sxs-lookup"><span data-stu-id="28003-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="28003-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="28003-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="28003-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="28003-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="28003-105">Вычисление Хадамард преобразования логической функции в {-1,1} кодировке с помощью метода Йейтса</span><span class="sxs-lookup"><span data-stu-id="28003-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="28003-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="28003-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="28003-107">Func: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="28003-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="28003-108">Истинная таблица в {-1,1} кодировке</span><span class="sxs-lookup"><span data-stu-id="28003-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="28003-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="28003-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="28003-110">Спектрал коэффициенты функции</span><span class="sxs-lookup"><span data-stu-id="28003-110">Spectral coefficients of the function</span></span>