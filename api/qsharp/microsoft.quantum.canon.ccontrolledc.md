---
uid: Microsoft.Quantum.Canon.CControlledC
title: Функция Кконтролледк
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledC
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 25ac2b35047b1c33a89149eae6d40f6f7ae3b454
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216920"
---
# <a name="ccontrolledc-function"></a><span data-ttu-id="71c79-102">Функция Кконтролледк</span><span class="sxs-lookup"><span data-stu-id="71c79-102">CControlledC function</span></span>

<span data-ttu-id="71c79-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="71c79-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="71c79-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="71c79-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="71c79-105">При наличии операции операция возвращает новую операцию, которая применяет оператор, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="71c79-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="71c79-106">Если `false` значение равно, ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="71c79-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="71c79-107">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="71c79-107">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
function CControlledC<'T> (op : ('T => Unit is Ctl)) : ((Bool, 'T) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="71c79-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="71c79-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="71c79-109">Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="71c79-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="71c79-110">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="71c79-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-ctl"></a><span data-ttu-id="71c79-111">Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL</span><span class="sxs-lookup"><span data-stu-id="71c79-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="71c79-112">Новая операция, выполняемая, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="71c79-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="71c79-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="71c79-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="71c79-114">Е</span><span class="sxs-lookup"><span data-stu-id="71c79-114">'T</span></span>

<span data-ttu-id="71c79-115">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="71c79-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="71c79-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="71c79-116">See Also</span></span>

- [<span data-ttu-id="71c79-117">Microsoft. тактов. Canon. Кконтроллед</span><span class="sxs-lookup"><span data-stu-id="71c79-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)