---
uid: Microsoft.Quantum.Logical.Xor
title: Функция XOR
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: ae43545e19e81ed5da17c3d58c62ac0b7ee765f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732816"
---
# <a name="xor-function"></a><span data-ttu-id="6bd2d-102">Функция XOR</span><span class="sxs-lookup"><span data-stu-id="6bd2d-102">Xor function</span></span>

<span data-ttu-id="6bd2d-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6bd2d-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6bd2d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6bd2d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6bd2d-105">Возвращает логическое исключающее сложение двух значений.</span><span class="sxs-lookup"><span data-stu-id="6bd2d-105">Returns the Boolean exclusive disjunction of two values.</span></span>

```qsharp
function Xor (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="6bd2d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6bd2d-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="6bd2d-107">ответ. [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6bd2d-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6bd2d-108">Первое значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="6bd2d-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="6bd2d-109">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="6bd2d-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6bd2d-110">Второе значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="6bd2d-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6bd2d-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6bd2d-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6bd2d-112">`true` только в том случае, если только один из них `a` `b` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="6bd2d-112">`true` if and only if exactly one of `a` and `b` is `true`.</span></span>