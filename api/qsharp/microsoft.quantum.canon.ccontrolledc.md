---
uid: Microsoft.Quantum.Canon.CControlledC
title: Функция Кконтролледк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledC
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: e5975455385e182236d7e2864e26ca00795a40c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716574"
---
# <a name="ccontrolledc-function"></a><span data-ttu-id="ef9c9-102">Функция Кконтролледк</span><span class="sxs-lookup"><span data-stu-id="ef9c9-102">CControlledC function</span></span>

<span data-ttu-id="ef9c9-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ef9c9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ef9c9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ef9c9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ef9c9-105">При наличии операции операция возвращает новую операцию, которая применяет оператор, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="ef9c9-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="ef9c9-106">Если `false` значение равно, ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="ef9c9-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="ef9c9-107">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="ef9c9-107">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
function CControlledC<'T> (op : ('T => Unit is Ctl)) : ((Bool, 'T) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="ef9c9-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ef9c9-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="ef9c9-109">Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="ef9c9-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="ef9c9-110">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="ef9c9-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit-ctl"></a><span data-ttu-id="ef9c9-111">Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) = Ctl [единицы](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="ef9c9-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="ef9c9-112">Новая операция, выполняемая, если классический контрольный бит имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="ef9c9-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ef9c9-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ef9c9-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ef9c9-114">Е</span><span class="sxs-lookup"><span data-stu-id="ef9c9-114">'T</span></span>

<span data-ttu-id="ef9c9-115">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="ef9c9-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef9c9-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="ef9c9-116">See Also</span></span>

- [<span data-ttu-id="ef9c9-117">Microsoft. тактов. Canon. Кконтроллед</span><span class="sxs-lookup"><span data-stu-id="ef9c9-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)