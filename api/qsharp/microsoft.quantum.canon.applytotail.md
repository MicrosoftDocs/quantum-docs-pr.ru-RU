---
uid: Microsoft.Quantum.Canon.ApplyToTail
title: Операция Апплитотаил
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTail
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 077e6dedee68b0bd05a668387b22f8bec87a4041
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850439"
---
# <a name="applytotail-operation"></a><span data-ttu-id="12961-102">Операция Апплитотаил</span><span class="sxs-lookup"><span data-stu-id="12961-102">ApplyToTail operation</span></span>

<span data-ttu-id="12961-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="12961-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="12961-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="12961-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="12961-105">Применяет операцию к последнему элементу массива.</span><span class="sxs-lookup"><span data-stu-id="12961-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTail<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="12961-106">Описание</span><span class="sxs-lookup"><span data-stu-id="12961-106">Description</span></span>

<span data-ttu-id="12961-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="12961-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="12961-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="12961-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="12961-109">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="12961-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="12961-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="12961-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="12961-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="12961-111">targets : 'T[]</span></span>

<span data-ttu-id="12961-112">Массив целевых объектов, к которым будет применен последний объект `op` .</span><span class="sxs-lookup"><span data-stu-id="12961-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="12961-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="12961-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="12961-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="12961-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="12961-115">Е</span><span class="sxs-lookup"><span data-stu-id="12961-115">'T</span></span>

<span data-ttu-id="12961-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="12961-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="12961-117">Пример</span><span class="sxs-lookup"><span data-stu-id="12961-117">Example</span></span>

<span data-ttu-id="12961-118">Следующие фрагменты кода Q # эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="12961-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToTail(H, register);
H(Tail(register));
```

## <a name="see-also"></a><span data-ttu-id="12961-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="12961-119">See Also</span></span>

- [<span data-ttu-id="12961-120">Microsoft. тактов. Canon. Апплитотаила</span><span class="sxs-lookup"><span data-stu-id="12961-120">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="12961-121">Microsoft. тактов. Canon. Апплитотаилк</span><span class="sxs-lookup"><span data-stu-id="12961-121">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="12961-122">Microsoft. тактов. Canon. Апплитотаилка</span><span class="sxs-lookup"><span data-stu-id="12961-122">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)