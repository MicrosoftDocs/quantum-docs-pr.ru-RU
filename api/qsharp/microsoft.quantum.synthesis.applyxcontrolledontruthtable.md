---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable
title: Операция Аппликсконтролледонтрустабле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTable
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 73d63936f02a52dfbbad7b8575110177a9e4463d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733929"
---
# <a name="applyxcontrolledontruthtable-operation"></a><span data-ttu-id="31400-102">Операция Аппликсконтролледонтрустабле</span><span class="sxs-lookup"><span data-stu-id="31400-102">ApplyXControlledOnTruthTable operation</span></span>

<span data-ttu-id="31400-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="31400-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="31400-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="31400-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="31400-105">Применяет @"microsoft.quantum.intrinsic.x" операцию к `target` , если логическая функция `func` возвращает значение true для классического назначения в `controlRegister` .</span><span class="sxs-lookup"><span data-stu-id="31400-105">Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.</span></span>

```qsharp
operation ApplyXControlledOnTruthTable (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="31400-106">Описание</span><span class="sxs-lookup"><span data-stu-id="31400-106">Description</span></span>

<span data-ttu-id="31400-107">Операция реализует единую операцию \бегин{алигн} У\кет {x} \ Сисакет {y} = \кет{КС}\кет{и \оплус f (x)} \енд{алигн}, где $x $ and $y $ представляют `controlRegister` и `target` соответственно.</span><span class="sxs-lookup"><span data-stu-id="31400-107">The operation implements the unitary operation \begin{align} U\ket{x}\ket{y} = \ket{x}\ket{y \oplus f(x)} \end{align} where $x$ and $y$ represent `controlRegister` and `target`, respectively.</span></span>

<span data-ttu-id="31400-108">Логическая функция $f $ представлена в виде таблицы истинности с точки зрения длинного целого числа.</span><span class="sxs-lookup"><span data-stu-id="31400-108">The Boolean function $f$ is represented as a truth table in terms of a big integer.</span></span>
<span data-ttu-id="31400-109">Например, функция большинства для трех входов представлена битстринг `11101000` , где наиболее значащий бит `1` соответствует назначению ввода `(1, 1, 1)` , а наименее значащий бит `0` соответствует назначению ввода `(0, 0, 0)` .</span><span class="sxs-lookup"><span data-stu-id="31400-109">For example, the majority function on three inputs is represented by the bitstring `11101000`, where the most significant bit `1` corresponds to the input assignment `(1, 1, 1)`, and the least significant bit `0` corresponds to the input assignment `(0, 0, 0)`.</span></span>
<span data-ttu-id="31400-110">Оно может представляться большим целым числом `0xE8L` в шестнадцатеричной нотации или `232L` в виде десятичной нотации.</span><span class="sxs-lookup"><span data-stu-id="31400-110">It can be represented by the big integer `0xE8L` in hexadecimal notation or as `232L` in decimal notation.</span></span>  <span data-ttu-id="31400-111">`L`Суффикс указывает, что константа имеет тип `BigInt` .</span><span class="sxs-lookup"><span data-stu-id="31400-111">The `L` suffix indicates that the constant is of type `BigInt`.</span></span>
<span data-ttu-id="31400-112">Дополнительные сведения об этом представлении можно найти в [таблице истинности Ката](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).</span><span class="sxs-lookup"><span data-stu-id="31400-112">More details on this representation can also be found in the [truth tables kata](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).</span></span>

<span data-ttu-id="31400-113">В реализации используются @"microsoft.quantum.intrinsic.cnot" @"microsoft.quantum.intrinsic.r1" шлюзы и.</span><span class="sxs-lookup"><span data-stu-id="31400-113">The implementation makes use of @"microsoft.quantum.intrinsic.cnot" and @"microsoft.quantum.intrinsic.r1" gates.</span></span>

## <a name="input"></a><span data-ttu-id="31400-114">Входные данные</span><span class="sxs-lookup"><span data-stu-id="31400-114">Input</span></span>

### <a name="func--bigint"></a><span data-ttu-id="31400-115">Func: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="31400-115">func : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="31400-116">Логическая таблица истинности, представленная как большое целое число</span><span class="sxs-lookup"><span data-stu-id="31400-116">Boolean truth table represented as big integer</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="31400-117">Контролрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="31400-117">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="31400-118">Регистрация элемента управления Кубитс</span><span class="sxs-lookup"><span data-stu-id="31400-118">Register of control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="31400-119">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="31400-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="31400-120">Целевой кубит</span><span class="sxs-lookup"><span data-stu-id="31400-120">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="31400-121">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="31400-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="31400-122">Ссылки</span><span class="sxs-lookup"><span data-stu-id="31400-122">References</span></span>

- [<span data-ttu-id="31400-123">*N. счуч* , *J. сиеверт* , прл 91, No 027902, 2003, арксив: Куант-pH/0303063</span><span class="sxs-lookup"><span data-stu-id="31400-123">*N. Schuch* , *J. Siewert* , PRL 91, no. 027902, 2003, arXiv:quant-ph/0303063</span></span>](https://arxiv.org/abs/quant-ph/0303063)
- [<span data-ttu-id="31400-124">*Матиас соекен* , *Мартен роеттелер* , арксив: 2005.12310</span><span class="sxs-lookup"><span data-stu-id="31400-124">*Mathias Soeken* , *Martin Roetteler* , arXiv:2005.12310</span></span>](https://arxiv.org/abs/2005.12310)

## <a name="see-also"></a><span data-ttu-id="31400-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="31400-125">See Also</span></span>

- [<span data-ttu-id="31400-126">Microsoft. тактов. синтез. Аппликсконтролледонтрустаблевисклеантаржет</span><span class="sxs-lookup"><span data-stu-id="31400-126">Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget)