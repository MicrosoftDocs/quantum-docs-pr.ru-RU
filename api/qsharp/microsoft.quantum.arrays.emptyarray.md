---
uid: Microsoft.Quantum.Arrays.EmptyArray
title: Функция Емптяррай
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EmptyArray
qsharp.summary: Returns the empty array of a given type.
ms.openlocfilehash: cf15e61862bb64fb3408db2318fafb56d532b365
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846173"
---
# <a name="emptyarray-function"></a><span data-ttu-id="77799-102">Функция Емптяррай</span><span class="sxs-lookup"><span data-stu-id="77799-102">EmptyArray function</span></span>

<span data-ttu-id="77799-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="77799-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="77799-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="77799-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="77799-105">Возвращает пустой массив заданного типа.</span><span class="sxs-lookup"><span data-stu-id="77799-105">Returns the empty array of a given type.</span></span>

```qsharp
function EmptyArray<'TElement> () : 'TElement[]
```


## <a name="output--telement"></a><span data-ttu-id="77799-106">Выходные данные: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="77799-106">Output : 'TElement[]</span></span>

<span data-ttu-id="77799-107">Пустой массив.</span><span class="sxs-lookup"><span data-stu-id="77799-107">The empty array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="77799-108">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="77799-108">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="77799-109">' TElement</span><span class="sxs-lookup"><span data-stu-id="77799-109">'TElement</span></span>

<span data-ttu-id="77799-110">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="77799-110">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="77799-111">Пример</span><span class="sxs-lookup"><span data-stu-id="77799-111">Example</span></span>

```qsharp
let empty = EmptyArray<Int>();
```