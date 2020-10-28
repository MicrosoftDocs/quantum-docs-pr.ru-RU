---
uid: Microsoft.Quantum.Canon.Fst
title: Функция ФСТ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 88ff5e29de9eeefcc1e207f277c37c63cb0faade
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716182"
---
# <a name="fst-function"></a><span data-ttu-id="525d7-102">Функция ФСТ</span><span class="sxs-lookup"><span data-stu-id="525d7-102">Fst function</span></span>

<span data-ttu-id="525d7-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="525d7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="525d7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="525d7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="525d7-105">При наличии пары возвращает ее первый элемент.</span><span class="sxs-lookup"><span data-stu-id="525d7-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="525d7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="525d7-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="525d7-107">пара: ('T, ' U)</span><span class="sxs-lookup"><span data-stu-id="525d7-107">pair : ('T,'U)</span></span>

<span data-ttu-id="525d7-108">Кортеж с двумя элементами.</span><span class="sxs-lookup"><span data-stu-id="525d7-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="525d7-109">Выходные данные: 'T</span><span class="sxs-lookup"><span data-stu-id="525d7-109">Output : 'T</span></span>

<span data-ttu-id="525d7-110">Первый элемент объекта `pair`.</span><span class="sxs-lookup"><span data-stu-id="525d7-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="525d7-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="525d7-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="525d7-112">Е</span><span class="sxs-lookup"><span data-stu-id="525d7-112">'T</span></span>

<span data-ttu-id="525d7-113">Тип первого элемента пары.</span><span class="sxs-lookup"><span data-stu-id="525d7-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="525d7-114">' U</span><span class="sxs-lookup"><span data-stu-id="525d7-114">'U</span></span>

<span data-ttu-id="525d7-115">Тип второго члена пары.</span><span class="sxs-lookup"><span data-stu-id="525d7-115">The type of the pair's second member.</span></span>