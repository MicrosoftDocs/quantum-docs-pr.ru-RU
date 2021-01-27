---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: Операция Каррйоуткорекдкм
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 2065c767b341241d32e5ac06bcff0071cbadb266
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843345"
---
# <a name="carryoutcorecdkm-operation"></a><span data-ttu-id="7d849-102">Операция Каррйоуткорекдкм</span><span class="sxs-lookup"><span data-stu-id="7d849-102">CarryOutCoreCDKM operation</span></span>

<span data-ttu-id="7d849-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7d849-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7d849-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7d849-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7d849-105">Основная операция в Рипплекарряддеркдкм, используемая с приведенной выше операцией Апплйоутеркдкмаддер, которая была сопряжена с этой операцией для получения внутренней операции Рипплекарряддеркдкм.</span><span class="sxs-lookup"><span data-stu-id="7d849-105">The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM.</span></span> <span data-ttu-id="7d849-106">Эта операция выполняет вычисление кубит и применяет последовательность нешлюзов для части входных данных `ys` .</span><span class="sxs-lookup"><span data-stu-id="7d849-106">This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.</span></span>

```qsharp
operation CarryOutCoreCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7d849-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7d849-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="7d849-108">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7d849-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7d849-109">Первый кубит регистр.</span><span class="sxs-lookup"><span data-stu-id="7d849-109">First qubit register.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="7d849-110">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7d849-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7d849-111">Второй кубит регистр.</span><span class="sxs-lookup"><span data-stu-id="7d849-111">Second qubit register.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="7d849-112">анЦилла: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7d849-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7d849-113">АнЦилла кубит, используемый в Рипплекарряддеркдкм, передан в эту операцию.</span><span class="sxs-lookup"><span data-stu-id="7d849-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="7d849-114">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7d849-114">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7d849-115">Выполните кубит в операции Рипплекарряддеркдкм.</span><span class="sxs-lookup"><span data-stu-id="7d849-115">Carry out qubit in the RippleCarryAdderCDKM operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7d849-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7d849-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="7d849-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="7d849-117">References</span></span>

- <span data-ttu-id="7d849-118">Андрей A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон: "Новая тактовая цепь Ripple — комплексное сложение", 2004.</span><span class="sxs-lookup"><span data-stu-id="7d849-118">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1