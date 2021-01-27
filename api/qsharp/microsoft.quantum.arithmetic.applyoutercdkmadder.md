---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: Операция Апплйоутеркдкмаддер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: acaa563245bb7c701316d2dfd35b5be03d8e024d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843704"
---
# <a name="applyoutercdkmadder-operation"></a><span data-ttu-id="735e3-102">Операция Апплйоутеркдкмаддер</span><span class="sxs-lookup"><span data-stu-id="735e3-102">ApplyOuterCDKMAdder operation</span></span>

<span data-ttu-id="735e3-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="735e3-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="735e3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="735e3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="735e3-105">Обратимая операция "Ripple" на месте, которая используется в операции сложения целых чисел, Рипплекарряддеркдкм ниже.</span><span class="sxs-lookup"><span data-stu-id="735e3-105">Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below.</span></span>
<span data-ttu-id="735e3-106">Учитывая два регистра кубит `xs` и `ys` одинаковую длину, операция применяет последовательность колебаний кнот и ккнот Gates с Кубитс в и, `xs` `ys` как элементы управления и Кубитс в `xs` качестве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="735e3-106">Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.</span></span>

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="735e3-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="735e3-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="735e3-108">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="735e3-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="735e3-109">Первый кубит регистр, содержащий элементы управления и целевые объекты.</span><span class="sxs-lookup"><span data-stu-id="735e3-109">First qubit register, containing controls and targets.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="735e3-110">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="735e3-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="735e3-111">Второй кубит регистр, участвующий в элементах управления.</span><span class="sxs-lookup"><span data-stu-id="735e3-111">Second qubit register, contributing to the controls.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="735e3-112">анЦилла: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="735e3-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="735e3-113">АнЦилла кубит, используемый в Рипплекарряддеркдкм, передан в эту операцию.</span><span class="sxs-lookup"><span data-stu-id="735e3-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="735e3-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="735e3-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="735e3-115">Ссылки</span><span class="sxs-lookup"><span data-stu-id="735e3-115">References</span></span>

- <span data-ttu-id="735e3-116">Андрей A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон: "Новая тактовая цепь Ripple — комплексное сложение", 2004.</span><span class="sxs-lookup"><span data-stu-id="735e3-116">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1