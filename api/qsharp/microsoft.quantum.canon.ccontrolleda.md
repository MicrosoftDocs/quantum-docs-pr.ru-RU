---
uid: Microsoft.Quantum.Canon.CControlledA
title: Функция Кконтролледа
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 823d80182621691f4fa6f42246b3d671f3adfc3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840994"
---
# <a name="ccontrolleda-function"></a><span data-ttu-id="c91ed-102">Функция Кконтролледа</span><span class="sxs-lookup"><span data-stu-id="c91ed-102">CControlledA function</span></span>

<span data-ttu-id="c91ed-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c91ed-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c91ed-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c91ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c91ed-105">При наличии операции операция возвращает новую операцию, которая применяет оператор, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="c91ed-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="c91ed-106">Если `false` значение равно, ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="c91ed-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="c91ed-107">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="c91ed-107">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="c91ed-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c91ed-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="c91ed-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="c91ed-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c91ed-110">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="c91ed-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-adj"></a><span data-ttu-id="c91ed-111">Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) => [единица](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c91ed-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c91ed-112">Новая операция, выполняемая, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="c91ed-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c91ed-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c91ed-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c91ed-114">Е</span><span class="sxs-lookup"><span data-stu-id="c91ed-114">'T</span></span>

<span data-ttu-id="c91ed-115">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="c91ed-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="c91ed-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="c91ed-116">See Also</span></span>

- [<span data-ttu-id="c91ed-117">Microsoft. тактов. Canon. Кконтроллед</span><span class="sxs-lookup"><span data-stu-id="c91ed-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)