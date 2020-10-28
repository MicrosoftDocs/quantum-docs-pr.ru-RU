---
uid: Microsoft.Quantum.Canon.CControlledA
title: Функция Кконтролледа
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 30b5e3408fa6e5a79b2f3d63cccc11899c0405ef
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716587"
---
# <a name="ccontrolleda-function"></a><span data-ttu-id="ad207-102">Функция Кконтролледа</span><span class="sxs-lookup"><span data-stu-id="ad207-102">CControlledA function</span></span>

<span data-ttu-id="ad207-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ad207-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ad207-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ad207-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ad207-105">При наличии операции операция возвращает новую операцию, которая применяет оператор, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="ad207-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="ad207-106">Если `false` значение равно, ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="ad207-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="ad207-107">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="ad207-107">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="ad207-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ad207-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="ad207-109">Op: 'T => [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ad207-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ad207-110">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="ad207-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit-adj"></a><span data-ttu-id="ad207-111">Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) = [>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="ad207-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ad207-112">Новая операция, выполняемая, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="ad207-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ad207-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ad207-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ad207-114">Е</span><span class="sxs-lookup"><span data-stu-id="ad207-114">'T</span></span>

<span data-ttu-id="ad207-115">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="ad207-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad207-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="ad207-116">See Also</span></span>

- [<span data-ttu-id="ad207-117">Microsoft. тактов. Canon. Кконтроллед</span><span class="sxs-lookup"><span data-stu-id="ad207-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)