---
uid: Microsoft.Quantum.Arrays.Tail
title: Tail, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Tail
qsharp.summary: Returns the last element of the array.
ms.openlocfilehash: 7a1eb2afefd662f90e58798b56bc83b34ac2abfd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729984"
---
# <a name="tail-function"></a><span data-ttu-id="7d495-102">Tail, функция</span><span class="sxs-lookup"><span data-stu-id="7d495-102">Tail function</span></span>

<span data-ttu-id="7d495-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7d495-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7d495-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7d495-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7d495-105">Возвращает последний элемент массива.</span><span class="sxs-lookup"><span data-stu-id="7d495-105">Returns the last element of the array.</span></span>

```qsharp
function Tail<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="7d495-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7d495-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="7d495-107">массив: ' A []</span><span class="sxs-lookup"><span data-stu-id="7d495-107">array : 'A[]</span></span>

<span data-ttu-id="7d495-108">Массив, в котором взят последний элемент.</span><span class="sxs-lookup"><span data-stu-id="7d495-108">Array of which the last element is taken.</span></span> <span data-ttu-id="7d495-109">Длина массива должна быть не меньше 1.</span><span class="sxs-lookup"><span data-stu-id="7d495-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="7d495-110">Выходные данные: ' A</span><span class="sxs-lookup"><span data-stu-id="7d495-110">Output : 'A</span></span>

<span data-ttu-id="7d495-111">Последний элемент массива.</span><span class="sxs-lookup"><span data-stu-id="7d495-111">The last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7d495-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7d495-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="7d495-113">' A</span><span class="sxs-lookup"><span data-stu-id="7d495-113">'A</span></span>

<span data-ttu-id="7d495-114">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="7d495-114">The type of the array elements.</span></span>