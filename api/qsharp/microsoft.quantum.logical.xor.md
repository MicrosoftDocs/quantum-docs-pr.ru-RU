---
uid: Microsoft.Quantum.Logical.Xor
title: Функция XOR
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: afb94bd1fd0b791a9a7d84bc28b0cc2baf9a0938
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197098"
---
# <a name="xor-function"></a><span data-ttu-id="8ab38-102">Функция XOR</span><span class="sxs-lookup"><span data-stu-id="8ab38-102">Xor function</span></span>

<span data-ttu-id="8ab38-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="8ab38-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="8ab38-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8ab38-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8ab38-105">Возвращает логическое исключающее сложение двух значений.</span><span class="sxs-lookup"><span data-stu-id="8ab38-105">Returns the Boolean exclusive disjunction of two values.</span></span>

```qsharp
function Xor (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="8ab38-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8ab38-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="8ab38-107">ответ. [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8ab38-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8ab38-108">Первое значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="8ab38-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="8ab38-109">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="8ab38-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8ab38-110">Второе значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="8ab38-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="8ab38-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8ab38-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8ab38-112">`true` только в том случае, если только один из них `a` `b` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="8ab38-112">`true` if and only if exactly one of `a` and `b` is `true`.</span></span>