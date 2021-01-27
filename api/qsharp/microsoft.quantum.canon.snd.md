---
uid: Microsoft.Quantum.Canon.Snd
title: Snd, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: 11786fa195de12a7f2e4f2edb00ac0bc1071dd5e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852150"
---
# <a name="snd-function"></a><span data-ttu-id="a21dd-102">Snd, функция</span><span class="sxs-lookup"><span data-stu-id="a21dd-102">Snd function</span></span>

<span data-ttu-id="a21dd-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a21dd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a21dd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a21dd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a21dd-105">При наличии пары возвращает второй элемент.</span><span class="sxs-lookup"><span data-stu-id="a21dd-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="a21dd-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a21dd-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="a21dd-107">пара: ('T, ' U)</span><span class="sxs-lookup"><span data-stu-id="a21dd-107">pair : ('T,'U)</span></span>

<span data-ttu-id="a21dd-108">Кортеж с двумя элементами.</span><span class="sxs-lookup"><span data-stu-id="a21dd-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="a21dd-109">Выходные данные: ' U</span><span class="sxs-lookup"><span data-stu-id="a21dd-109">Output : 'U</span></span>

<span data-ttu-id="a21dd-110">Второй элемент `pair` .</span><span class="sxs-lookup"><span data-stu-id="a21dd-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a21dd-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a21dd-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a21dd-112">Е</span><span class="sxs-lookup"><span data-stu-id="a21dd-112">'T</span></span>

<span data-ttu-id="a21dd-113">Тип первого элемента пары.</span><span class="sxs-lookup"><span data-stu-id="a21dd-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="a21dd-114">' U</span><span class="sxs-lookup"><span data-stu-id="a21dd-114">'U</span></span>

<span data-ttu-id="a21dd-115">Тип второго члена пары.</span><span class="sxs-lookup"><span data-stu-id="a21dd-115">The type of the pair's second member.</span></span>