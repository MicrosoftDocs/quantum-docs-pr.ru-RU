---
uid: Microsoft.Quantum.Canon.ApplyToRest
title: Операция Апплиторест
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRest
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: f18536a056935220feedc4ea50531c5def61d650
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850508"
---
# <a name="applytorest-operation"></a><span data-ttu-id="a3523-102">Операция Апплиторест</span><span class="sxs-lookup"><span data-stu-id="a3523-102">ApplyToRest operation</span></span>

<span data-ttu-id="a3523-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a3523-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a3523-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a3523-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a3523-105">Применяет операцию ко всему элементу массива, кроме первого элемента.</span><span class="sxs-lookup"><span data-stu-id="a3523-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRest<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="a3523-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a3523-106">Description</span></span>

<span data-ttu-id="a3523-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="a3523-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="a3523-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a3523-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="a3523-109">Op: 'T [] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="a3523-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a3523-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="a3523-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="a3523-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="a3523-111">targets : 'T[]</span></span>

<span data-ttu-id="a3523-112">Массив целевых объектов, к которым будут применяться все, кроме первого `op` .</span><span class="sxs-lookup"><span data-stu-id="a3523-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a3523-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a3523-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a3523-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a3523-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a3523-115">Е</span><span class="sxs-lookup"><span data-stu-id="a3523-115">'T</span></span>

<span data-ttu-id="a3523-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="a3523-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="a3523-117">Пример</span><span class="sxs-lookup"><span data-stu-id="a3523-117">Example</span></span>

<span data-ttu-id="a3523-118">Следующие фрагменты кода Q # эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="a3523-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToRest(ApplyCNOTChain, register);
ApplyCNOTChain(Rest(register));
```

## <a name="see-also"></a><span data-ttu-id="a3523-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="a3523-119">See Also</span></span>

- [<span data-ttu-id="a3523-120">Microsoft. тактов. Canon. Апплитореста</span><span class="sxs-lookup"><span data-stu-id="a3523-120">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="a3523-121">Microsoft. тактов. Canon. Апплиторестк</span><span class="sxs-lookup"><span data-stu-id="a3523-121">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="a3523-122">Microsoft. тактов. Canon. Апплиторестка</span><span class="sxs-lookup"><span data-stu-id="a3523-122">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)