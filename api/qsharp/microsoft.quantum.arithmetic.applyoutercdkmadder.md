---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: Операция Апплйоутеркдкмаддер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: 5ec9d31252254e40efb22e06656294325b4cffcd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731816"
---
# <a name="applyoutercdkmadder-operation"></a><span data-ttu-id="a4d2c-102">Операция Апплйоутеркдкмаддер</span><span class="sxs-lookup"><span data-stu-id="a4d2c-102">ApplyOuterCDKMAdder operation</span></span>

<span data-ttu-id="a4d2c-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a4d2c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a4d2c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a4d2c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a4d2c-105">Обратимая операция "Ripple" на месте, которая используется в операции сложения целых чисел, Рипплекарряддеркдкм ниже.</span><span class="sxs-lookup"><span data-stu-id="a4d2c-105">Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below.</span></span>
<span data-ttu-id="a4d2c-106">Учитывая два регистра кубит `xs` и `ys` одинаковую длину, операция применяет последовательность колебаний кнот и ккнот Gates с Кубитс в и, `xs` `ys` как элементы управления и Кубитс в `xs` качестве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="a4d2c-106">Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.</span></span>

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="a4d2c-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a4d2c-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="a4d2c-108">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a4d2c-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a4d2c-109">Первый кубит регистр, содержащий элементы управления и целевые объекты.</span><span class="sxs-lookup"><span data-stu-id="a4d2c-109">First qubit register, containing controls and targets.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="a4d2c-110">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a4d2c-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a4d2c-111">Второй кубит регистр, участвующий в элементах управления.</span><span class="sxs-lookup"><span data-stu-id="a4d2c-111">Second qubit register, contributing to the controls.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="a4d2c-112">анЦилла: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a4d2c-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a4d2c-113">АнЦилла кубит, используемый в Рипплекарряддеркдкм, передан в эту операцию.</span><span class="sxs-lookup"><span data-stu-id="a4d2c-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a4d2c-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a4d2c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="a4d2c-115">Ссылки</span><span class="sxs-lookup"><span data-stu-id="a4d2c-115">References</span></span>

- <span data-ttu-id="a4d2c-116">Андрей A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон: "Новая тактовая цепь Ripple — комплексное сложение", 2004.</span><span class="sxs-lookup"><span data-stu-id="a4d2c-116">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1