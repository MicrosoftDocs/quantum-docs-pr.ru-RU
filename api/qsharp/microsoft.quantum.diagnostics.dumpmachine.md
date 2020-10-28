---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: Функция Думпмачине
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: c85cf6764bdc913a71448c525318f45743bf1df0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712877"
---
# <a name="dumpmachine-function"></a><span data-ttu-id="9a6d6-102">Функция Думпмачине</span><span class="sxs-lookup"><span data-stu-id="9a6d6-102">DumpMachine function</span></span>

<span data-ttu-id="9a6d6-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="9a6d6-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="9a6d6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9a6d6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9a6d6-105">Выводит дамп текущего состояния целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-105">Dumps the current target machine's status.</span></span>

```qsharp
function DumpMachine<'T> (location : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="9a6d6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9a6d6-106">Input</span></span>

### <a name="location--t"></a><span data-ttu-id="9a6d6-107">Расположение: не</span><span class="sxs-lookup"><span data-stu-id="9a6d6-107">location : 'T</span></span>

<span data-ttu-id="9a6d6-108">Содержит сведения о том, где создать дамп компьютера.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-108">Provides information on where to generate the machine's dump.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9a6d6-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9a6d6-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="9a6d6-110">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-110">None.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9a6d6-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="9a6d6-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9a6d6-112">Е</span><span class="sxs-lookup"><span data-stu-id="9a6d6-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="9a6d6-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="9a6d6-113">Remarks</span></span>

<span data-ttu-id="9a6d6-114">Этот метод позволяет вывести сведения о текущем состоянии целевого компьютера в файл или в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-114">This method allows you to dump information about the current status of the target machine into a file or some other location.</span></span>
<span data-ttu-id="9a6d6-115">Фактически сформированные сведения и семантика `location` относятся к каждому целевому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-115">The actual information generated and the semantics of `location` are specific to each target machine.</span></span> <span data-ttu-id="9a6d6-116">Однако предоставление пустого кортежа в качестве расположения ( `()` ) или просто пропуск `location` параметра обычно означает создание выходных данных в консоли.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-116">However, providing an empty tuple as a location (`()`) or just omitting the `location` parameter typically means to generate the output to the console.</span></span>

<span data-ttu-id="9a6d6-117">Для локального симулятора полного состояния, распространяемого в составе пакета средств разработки такта, этот метод ожидает строку с путем к файлу, в котором она будет записывать функцию Wave как одномерный массив комплексных чисел, в котором каждый элемент представляет амплитуды вероятности измерения соответствующего состояния.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-117">For the local full state simulator distributed as part of the Quantum Development Kit, this method  expects a string with the path to a file in which it will write the wave function as a one-dimensional array of complex numbers, in which each element represents the amplitudes of the probability of measuring the corresponding state.</span></span>