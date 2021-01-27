---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Функция Фассадамардтрансформед
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: be54413ef2d3fdaf7ddc726bc0906adb4ec382ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855449"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="5240e-102">Функция Фассадамардтрансформед</span><span class="sxs-lookup"><span data-stu-id="5240e-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="5240e-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="5240e-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="5240e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5240e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5240e-105">Вычисление Хадамард преобразования логической функции в {-1,1} кодировке с помощью метода Йейтса</span><span class="sxs-lookup"><span data-stu-id="5240e-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="5240e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5240e-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="5240e-107">Func: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5240e-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5240e-108">Истинная таблица в {-1,1} кодировке</span><span class="sxs-lookup"><span data-stu-id="5240e-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="5240e-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5240e-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5240e-110">Спектрал коэффициенты функции</span><span class="sxs-lookup"><span data-stu-id="5240e-110">Spectral coefficients of the function</span></span>

## <a name="example"></a><span data-ttu-id="5240e-111">Пример</span><span class="sxs-lookup"><span data-stu-id="5240e-111">Example</span></span>

```qsharp
FastHadamardTransformed([1, 1, 1, -1]); // [2, 2, 2, -2]
```