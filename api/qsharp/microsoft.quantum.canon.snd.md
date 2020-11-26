---
uid: Microsoft.Quantum.Canon.Snd
title: Snd, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: c935a2bc9e3f5ab32669feae2bfc0f2ebf57e744
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205326"
---
# <a name="snd-function"></a><span data-ttu-id="a69a9-102">Snd, функция</span><span class="sxs-lookup"><span data-stu-id="a69a9-102">Snd function</span></span>

<span data-ttu-id="a69a9-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a69a9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a69a9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a69a9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a69a9-105">При наличии пары возвращает второй элемент.</span><span class="sxs-lookup"><span data-stu-id="a69a9-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="a69a9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a69a9-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="a69a9-107">пара: ('T, ' U)</span><span class="sxs-lookup"><span data-stu-id="a69a9-107">pair : ('T,'U)</span></span>

<span data-ttu-id="a69a9-108">Кортеж с двумя элементами.</span><span class="sxs-lookup"><span data-stu-id="a69a9-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="a69a9-109">Выходные данные: ' U</span><span class="sxs-lookup"><span data-stu-id="a69a9-109">Output : 'U</span></span>

<span data-ttu-id="a69a9-110">Второй элемент `pair` .</span><span class="sxs-lookup"><span data-stu-id="a69a9-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a69a9-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a69a9-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a69a9-112">Е</span><span class="sxs-lookup"><span data-stu-id="a69a9-112">'T</span></span>

<span data-ttu-id="a69a9-113">Тип первого элемента пары.</span><span class="sxs-lookup"><span data-stu-id="a69a9-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="a69a9-114">' U</span><span class="sxs-lookup"><span data-stu-id="a69a9-114">'U</span></span>

<span data-ttu-id="a69a9-115">Тип второго члена пары.</span><span class="sxs-lookup"><span data-stu-id="a69a9-115">The type of the pair's second member.</span></span>