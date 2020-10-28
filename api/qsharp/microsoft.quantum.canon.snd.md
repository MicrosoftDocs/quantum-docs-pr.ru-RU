---
uid: Microsoft.Quantum.Canon.Snd
title: Snd, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: c05053b45d24c3398526d1269b90bb40d1e0ef27
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715453"
---
# <a name="snd-function"></a><span data-ttu-id="d2052-102">Snd, функция</span><span class="sxs-lookup"><span data-stu-id="d2052-102">Snd function</span></span>

<span data-ttu-id="d2052-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d2052-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d2052-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d2052-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d2052-105">При наличии пары возвращает второй элемент.</span><span class="sxs-lookup"><span data-stu-id="d2052-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="d2052-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d2052-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="d2052-107">пара: ('T, ' U)</span><span class="sxs-lookup"><span data-stu-id="d2052-107">pair : ('T,'U)</span></span>

<span data-ttu-id="d2052-108">Кортеж с двумя элементами.</span><span class="sxs-lookup"><span data-stu-id="d2052-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="d2052-109">Выходные данные: ' U</span><span class="sxs-lookup"><span data-stu-id="d2052-109">Output : 'U</span></span>

<span data-ttu-id="d2052-110">Второй элемент `pair` .</span><span class="sxs-lookup"><span data-stu-id="d2052-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d2052-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="d2052-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d2052-112">Е</span><span class="sxs-lookup"><span data-stu-id="d2052-112">'T</span></span>

<span data-ttu-id="d2052-113">Тип первого элемента пары.</span><span class="sxs-lookup"><span data-stu-id="d2052-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="d2052-114">' U</span><span class="sxs-lookup"><span data-stu-id="d2052-114">'U</span></span>

<span data-ttu-id="d2052-115">Тип второго члена пары.</span><span class="sxs-lookup"><span data-stu-id="d2052-115">The type of the pair's second member.</span></span>