---
uid: Microsoft.Quantum.Diagnostics.DumpRegister
title: Функция Думпрегистер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpRegister
qsharp.summary: Dumps the current target machine's status associated with the given qubits.
ms.openlocfilehash: a6d29dbf0525077fd804563f85f189740fdc0429
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712836"
---
# <a name="dumpregister-function"></a><span data-ttu-id="61166-102">Функция Думпрегистер</span><span class="sxs-lookup"><span data-stu-id="61166-102">DumpRegister function</span></span>

<span data-ttu-id="61166-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="61166-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="61166-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="61166-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="61166-105">Выводит состояние текущего целевого компьютера, связанного с заданным Кубитс.</span><span class="sxs-lookup"><span data-stu-id="61166-105">Dumps the current target machine's status associated with the given qubits.</span></span>

```qsharp
function DumpRegister<'T> (location : 'T, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="61166-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="61166-106">Input</span></span>

### <a name="location--t"></a><span data-ttu-id="61166-107">Расположение: не</span><span class="sxs-lookup"><span data-stu-id="61166-107">location : 'T</span></span>

<span data-ttu-id="61166-108">Содержит сведения о том, где можно создать дамп состояния.</span><span class="sxs-lookup"><span data-stu-id="61166-108">Provides information on where to generate the state's dump.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="61166-109">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="61166-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="61166-110">Список Кубитс для отчета.</span><span class="sxs-lookup"><span data-stu-id="61166-110">The list of qubits to report.</span></span>



## <a name="output--unit"></a><span data-ttu-id="61166-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="61166-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="61166-112">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="61166-112">None.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="61166-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="61166-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="61166-114">Е</span><span class="sxs-lookup"><span data-stu-id="61166-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="61166-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="61166-115">Remarks</span></span>

<span data-ttu-id="61166-116">Этот метод позволяет сохранить дамп сведений, связанных с состоянием заданного Кубитс, в файл или в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="61166-116">This method allows you to dump the information associated with the state of the given qubits into a file or some other location.</span></span>
<span data-ttu-id="61166-117">Фактически сформированные сведения и семантика `location` относятся к каждому целевому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="61166-117">The actual information generated and the semantics of `location` are specific to each target machine.</span></span> <span data-ttu-id="61166-118">Однако предоставление пустого кортежа в качестве расположения ( `()` ) обычно означает создание выходных данных в консоли.</span><span class="sxs-lookup"><span data-stu-id="61166-118">However, providing an empty tuple as a location (`()`) typically means to generate the output to the console.</span></span>

<span data-ttu-id="61166-119">Для локального симулятора полного состояния, распространяемого в составе пакета средств разработки тактов, этот метод ожидает строку с путем к файлу, в котором он будет записывать состояние данного Кубитс (т. е. Функция Wave соответствующей подсистемы) как одномерный массив комплексных чисел, в котором каждый элемент представляет амплитуды вероятности измерения соответствующего состояния.</span><span class="sxs-lookup"><span data-stu-id="61166-119">For the local full state simulator distributed as part of the Quantum Development Kit, this method  expects a string with the path to a file in which it will write the state of the given qubits (i.e. the wave function of the corresponding  subsystem) as a one-dimensional array of complex numbers, in which each element represents the amplitudes of the probability of measuring the corresponding state.</span></span>
<span data-ttu-id="61166-120">Если заданный Кубитс запутанными с другим кубит и их состояние нельзя разделить, то просто сообщает, что Кубитс являются запутанными.</span><span class="sxs-lookup"><span data-stu-id="61166-120">If the given qubits are entangled with some other qubit and their state can't be separated, it just reports that the qubits are entangled.</span></span>