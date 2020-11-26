---
uid: Microsoft.Quantum.Canon.Fst
title: Функция ФСТ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 634f11881a054df7fe79d889832ea6bd80a7394f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206941"
---
# <a name="fst-function"></a><span data-ttu-id="f70de-102">Функция ФСТ</span><span class="sxs-lookup"><span data-stu-id="f70de-102">Fst function</span></span>

<span data-ttu-id="f70de-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f70de-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f70de-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f70de-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f70de-105">При наличии пары возвращает ее первый элемент.</span><span class="sxs-lookup"><span data-stu-id="f70de-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="f70de-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f70de-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="f70de-107">пара: ('T, ' U)</span><span class="sxs-lookup"><span data-stu-id="f70de-107">pair : ('T,'U)</span></span>

<span data-ttu-id="f70de-108">Кортеж с двумя элементами.</span><span class="sxs-lookup"><span data-stu-id="f70de-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="f70de-109">Выходные данные: 'T</span><span class="sxs-lookup"><span data-stu-id="f70de-109">Output : 'T</span></span>

<span data-ttu-id="f70de-110">Первый элемент объекта `pair`.</span><span class="sxs-lookup"><span data-stu-id="f70de-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f70de-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="f70de-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f70de-112">Е</span><span class="sxs-lookup"><span data-stu-id="f70de-112">'T</span></span>

<span data-ttu-id="f70de-113">Тип первого элемента пары.</span><span class="sxs-lookup"><span data-stu-id="f70de-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="f70de-114">' U</span><span class="sxs-lookup"><span data-stu-id="f70de-114">'U</span></span>

<span data-ttu-id="f70de-115">Тип второго члена пары.</span><span class="sxs-lookup"><span data-stu-id="f70de-115">The type of the pair's second member.</span></span>