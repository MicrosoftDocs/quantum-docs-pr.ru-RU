---
uid: Microsoft.Quantum.Canon.CControlled
title: Функция Кконтроллед
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlled
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens.
ms.openlocfilehash: a155b00806b17258b3f87629659bc7d786e4e11d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716588"
---
# <a name="ccontrolled-function"></a><span data-ttu-id="a8c70-102">Функция Кконтроллед</span><span class="sxs-lookup"><span data-stu-id="a8c70-102">CControlled function</span></span>

<span data-ttu-id="a8c70-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a8c70-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a8c70-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a8c70-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a8c70-105">При наличии операции операция возвращает новую операцию, которая применяет оператор, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="a8c70-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="a8c70-106">Если `false` значение равно, ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="a8c70-106">If `false`, nothing happens.</span></span>

```qsharp
function CControlled<'T> (op : ('T => Unit)) : ((Bool, 'T) => Unit)
```


## <a name="input"></a><span data-ttu-id="a8c70-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a8c70-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="a8c70-108">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="a8c70-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a8c70-109">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="a8c70-109">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit"></a><span data-ttu-id="a8c70-110">Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="a8c70-110">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a8c70-111">Новая операция, выполняемая, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="a8c70-111">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a8c70-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a8c70-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a8c70-113">Е</span><span class="sxs-lookup"><span data-stu-id="a8c70-113">'T</span></span>

<span data-ttu-id="a8c70-114">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="a8c70-114">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8c70-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="a8c70-115">See Also</span></span>

- [<span data-ttu-id="a8c70-116">Microsoft. тактов. Canon. Кконтролледк</span><span class="sxs-lookup"><span data-stu-id="a8c70-116">Microsoft.Quantum.Canon.CControlledC</span></span>](xref:Microsoft.Quantum.Canon.CControlledC)
- [<span data-ttu-id="a8c70-117">Microsoft. тактов. Canon. Кконтролледа</span><span class="sxs-lookup"><span data-stu-id="a8c70-117">Microsoft.Quantum.Canon.CControlledA</span></span>](xref:Microsoft.Quantum.Canon.CControlledA)
- [<span data-ttu-id="a8c70-118">Microsoft. тактов. Canon. Кконтролледка</span><span class="sxs-lookup"><span data-stu-id="a8c70-118">Microsoft.Quantum.Canon.CControlledCA</span></span>](xref:Microsoft.Quantum.Canon.CControlledCA)