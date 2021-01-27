---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: Функция Блоккенкодингбилку
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 1d7890e96513817c127ef768f49c0b915ea22fa1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858157"
---
# <a name="blockencodingbylcu-function"></a><span data-ttu-id="ba781-102">Функция Блоккенкодингбилку</span><span class="sxs-lookup"><span data-stu-id="ba781-102">BlockEncodingByLCU function</span></span>

<span data-ttu-id="ba781-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ba781-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ba781-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ba781-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ba781-105">Кодирует интересующий оператор в `BlockEncoding` .</span><span class="sxs-lookup"><span data-stu-id="ba781-105">Encodes an operator of interest into a `BlockEncoding`.</span></span>

<span data-ttu-id="ba781-106">Создается `BlockEncoding` единая $U = П\кдот В\кдот P ^ \дагжер $, которая кодирует некоторый оператор $H = \ sum_ {j} | \ alpha_j | U_j $, представляющая собой линейное сочетание унитариес.</span><span class="sxs-lookup"><span data-stu-id="ba781-106">This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="ba781-107">Как правило, $P $ является подготовкой состояния, таким, что $P \кет {0} \_ a = \ sum_j \скрт{\ alpha_j/ \| \век\алфа \| \_ 2} \кет{ж} \_ a $ и $V = \ sum_ {j} \кет{ж}\бра{ж} \_ а\отимес U_j $.</span><span class="sxs-lookup"><span data-stu-id="ba781-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="ba781-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ba781-108">Input</span></span>

### <a name="statepreparation--t--unit--is-adj--ctl"></a><span data-ttu-id="ba781-109">Статепрепаратион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="ba781-109">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ba781-110">Единое $P $, которое готовит конечное состояние.</span><span class="sxs-lookup"><span data-stu-id="ba781-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--ts--unit--is-adj--ctl"></a><span data-ttu-id="ba781-111">селектор: ('T) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="ba781-111">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ba781-112">Единое $V $, которое кодирует компонент унитариес $H $.</span><span class="sxs-lookup"><span data-stu-id="ba781-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--ts--unit--is-adj--ctl"></a><span data-ttu-id="ba781-113">Выходные данные: ('T) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="ba781-113">Output : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ba781-114">Единая $U $ взаимодействует с регистрами `a` и `s` кодирует $H $ и соответствует $U ^ \Дагжер = U $.</span><span class="sxs-lookup"><span data-stu-id="ba781-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U^\dagger = U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ba781-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ba781-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ba781-116">Е</span><span class="sxs-lookup"><span data-stu-id="ba781-116">'T</span></span>


### <a name="s"></a><span data-ttu-id="ba781-117">Возникл</span><span class="sxs-lookup"><span data-stu-id="ba781-117">'S</span></span>



## <a name="remarks"></a><span data-ttu-id="ba781-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="ba781-118">Remarks</span></span>

<span data-ttu-id="ba781-119">Эта `BlockEncoding` Реализация предоставляет ей свойства `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="ba781-119">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba781-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="ba781-120">See Also</span></span>

- [<span data-ttu-id="ba781-121">Microsoft. тактов. моделирование. Блоккенкодинг</span><span class="sxs-lookup"><span data-stu-id="ba781-121">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="ba781-122">Microsoft. тактов. моделирование. Блоккенкодингрефлектион</span><span class="sxs-lookup"><span data-stu-id="ba781-122">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)