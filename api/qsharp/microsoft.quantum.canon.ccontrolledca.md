---
uid: Microsoft.Quantum.Canon.CControlledCA
title: Функция Кконтролледка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledCA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 740461ee17bdda281a6bd8572a15d27b17be9535
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840949"
---
# <a name="ccontrolledca-function"></a><span data-ttu-id="50015-102">Функция Кконтролледка</span><span class="sxs-lookup"><span data-stu-id="50015-102">CControlledCA function</span></span>

<span data-ttu-id="50015-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="50015-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="50015-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="50015-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="50015-105">При наличии операции операция возвращает новую операцию, которая применяет оператор, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="50015-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="50015-106">Если `false` значение равно, ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="50015-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="50015-107">Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="50015-107">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
function CControlledCA<'T> (op : ('T => Unit is Ctl + Adj)) : ((Bool, 'T) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="50015-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="50015-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="50015-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="50015-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="50015-110">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="50015-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-adj--ctl"></a><span data-ttu-id="50015-111">Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="50015-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="50015-112">Новая операция, выполняемая, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="50015-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="50015-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="50015-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="50015-114">Е</span><span class="sxs-lookup"><span data-stu-id="50015-114">'T</span></span>

<span data-ttu-id="50015-115">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="50015-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="50015-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="50015-116">See Also</span></span>

- [<span data-ttu-id="50015-117">Microsoft. тактов. Canon. Кконтроллед</span><span class="sxs-lookup"><span data-stu-id="50015-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)