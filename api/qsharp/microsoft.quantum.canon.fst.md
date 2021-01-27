---
uid: Microsoft.Quantum.Canon.Fst
title: Функция ФСТ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: cd5746358c8323f8d2dbca44965fa5dbac0a84c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840514"
---
# <a name="fst-function"></a><span data-ttu-id="e00ed-102">Функция ФСТ</span><span class="sxs-lookup"><span data-stu-id="e00ed-102">Fst function</span></span>

<span data-ttu-id="e00ed-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e00ed-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e00ed-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e00ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e00ed-105">При наличии пары возвращает ее первый элемент.</span><span class="sxs-lookup"><span data-stu-id="e00ed-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="e00ed-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e00ed-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="e00ed-107">пара: ('T, ' U)</span><span class="sxs-lookup"><span data-stu-id="e00ed-107">pair : ('T,'U)</span></span>

<span data-ttu-id="e00ed-108">Кортеж с двумя элементами.</span><span class="sxs-lookup"><span data-stu-id="e00ed-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="e00ed-109">Выходные данные: 'T</span><span class="sxs-lookup"><span data-stu-id="e00ed-109">Output : 'T</span></span>

<span data-ttu-id="e00ed-110">Первый элемент объекта `pair`.</span><span class="sxs-lookup"><span data-stu-id="e00ed-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e00ed-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e00ed-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e00ed-112">Е</span><span class="sxs-lookup"><span data-stu-id="e00ed-112">'T</span></span>

<span data-ttu-id="e00ed-113">Тип первого элемента пары.</span><span class="sxs-lookup"><span data-stu-id="e00ed-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="e00ed-114">' U</span><span class="sxs-lookup"><span data-stu-id="e00ed-114">'U</span></span>

<span data-ttu-id="e00ed-115">Тип второго члена пары.</span><span class="sxs-lookup"><span data-stu-id="e00ed-115">The type of the pair's second member.</span></span>