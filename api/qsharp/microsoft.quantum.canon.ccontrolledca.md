---
uid: Microsoft.Quantum.Canon.CControlledCA
title: Функция Кконтролледка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledCA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 20a8c9ccf931261f7bc6e347ccc144c92f0d0545
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716573"
---
# <a name="ccontrolledca-function"></a><span data-ttu-id="9eb1a-102">Функция Кконтролледка</span><span class="sxs-lookup"><span data-stu-id="9eb1a-102">CControlledCA function</span></span>

<span data-ttu-id="9eb1a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9eb1a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9eb1a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9eb1a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9eb1a-105">При наличии операции операция возвращает новую операцию, которая применяет оператор, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="9eb1a-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="9eb1a-106">Если `false` значение равно, ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="9eb1a-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="9eb1a-107">Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="9eb1a-107">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
function CControlledCA<'T> (op : ('T => Unit is Ctl + Adj)) : ((Bool, 'T) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="9eb1a-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9eb1a-108">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="9eb1a-109">Op: t => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные</span><span class="sxs-lookup"><span data-stu-id="9eb1a-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="9eb1a-110">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="9eb1a-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit-ctl--adj"></a><span data-ttu-id="9eb1a-111">Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные</span><span class="sxs-lookup"><span data-stu-id="9eb1a-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="9eb1a-112">Новая операция, выполняемая, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="9eb1a-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9eb1a-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="9eb1a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9eb1a-114">Е</span><span class="sxs-lookup"><span data-stu-id="9eb1a-114">'T</span></span>

<span data-ttu-id="9eb1a-115">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="9eb1a-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="9eb1a-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="9eb1a-116">See Also</span></span>

- [<span data-ttu-id="9eb1a-117">Microsoft. тактов. Canon. Кконтроллед</span><span class="sxs-lookup"><span data-stu-id="9eb1a-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)