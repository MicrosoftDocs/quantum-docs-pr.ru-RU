---
uid: Microsoft.Quantum.Simulation.BlockEncodingReflectionByLCU
title: Функция Блоккенкодингрефлектионбилку
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingReflectionByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncodingReflection`.

  This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: b8eff9d207752213ccdf42a9ad80fefb2da07216
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733169"
---
# <a name="blockencodingreflectionbylcu-function"></a><span data-ttu-id="a4250-102">Функция Блоккенкодингрефлектионбилку</span><span class="sxs-lookup"><span data-stu-id="a4250-102">BlockEncodingReflectionByLCU function</span></span>

<span data-ttu-id="a4250-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="a4250-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="a4250-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a4250-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a4250-105">Кодирует интересующий оператор в `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="a4250-105">Encodes an operator of interest into a `BlockEncodingReflection`.</span></span>

<span data-ttu-id="a4250-106">Создается `BlockEncodingReflection` единая $U = П\кдот В\кдот P ^ \дагжер $, которая кодирует некоторый оператор $H = \ sum_ {j} | \ alpha_j | U_j $, представляющая собой линейное сочетание унитариес.</span><span class="sxs-lookup"><span data-stu-id="a4250-106">This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="a4250-107">Как правило, $P $ является подготовкой состояния, таким, что $P \кет {0} \_ a \ sum_j alpha_j \скрт{\/ \| \век\алфа \| \_ 2} \кет{ж} \_ a $ и $V = \ sum_ {j} \кет{ж}\бра{ж} \_ а\отимес U_j $.</span><span class="sxs-lookup"><span data-stu-id="a4250-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingReflectionByLCU (statePreparation : (Qubit[] => Unit is Adj + Ctl), selector : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a><span data-ttu-id="a4250-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a4250-108">Input</span></span>

### <a name="statepreparation--qubit--unit-adj--ctl"></a><span data-ttu-id="a4250-109">Статепрепаратион: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="a4250-109">statePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="a4250-110">Единое $P $, которое готовит конечное состояние.</span><span class="sxs-lookup"><span data-stu-id="a4250-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--qubitqubit--unit-adj--ctl"></a><span data-ttu-id="a4250-111">селектор: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) [=>ная](xref:microsoft.quantum.lang-ref.unit) расгода и CTL</span><span class="sxs-lookup"><span data-stu-id="a4250-111">selector : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="a4250-112">Единое $V $, которое кодирует компонент унитариес $H $.</span><span class="sxs-lookup"><span data-stu-id="a4250-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--blockencodingreflection"></a><span data-ttu-id="a4250-113">Выходные данные: [блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="a4250-113">Output : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="a4250-114">Единая $U $, взаимодействующая с регистрами `a` и `s` которая кодирует $H $, и соответствует $U "^ {-1} = U $.</span><span class="sxs-lookup"><span data-stu-id="a4250-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U'^{-1} = U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4250-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="a4250-115">Remarks</span></span>

<span data-ttu-id="a4250-116">Эта `BlockEncoding` Реализация предоставляет ей свойства `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="a4250-116">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4250-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="a4250-117">See Also</span></span>

- [<span data-ttu-id="a4250-118">Microsoft. тактов. моделирование. Блоккенкодинг</span><span class="sxs-lookup"><span data-stu-id="a4250-118">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="a4250-119">Microsoft. тактов. моделирование. Блоккенкодингрефлектион</span><span class="sxs-lookup"><span data-stu-id="a4250-119">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)