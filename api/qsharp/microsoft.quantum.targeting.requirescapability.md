---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: Определяемый пользователем тип Рекуирескапабилити
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 63b1952d402f1bcb81a8f9d0afc3cdf7aa7e5ed8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733865"
---
# <a name="requirescapability-user-defined-type"></a><span data-ttu-id="313d2-102">Определяемый пользователем тип Рекуирескапабилити</span><span class="sxs-lookup"><span data-stu-id="313d2-102">RequiresCapability user defined type</span></span>

<span data-ttu-id="313d2-103">Пространство имен: [Microsoft. тактов. нацеливание](xref:Microsoft.Quantum.Targeting)</span><span class="sxs-lookup"><span data-stu-id="313d2-103">Namespace: [Microsoft.Quantum.Targeting](xref:Microsoft.Quantum.Targeting)</span></span>

<span data-ttu-id="313d2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="313d2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="313d2-105">Распознанный компилятором атрибут, используемый для пометки вызываемого с возможностями среды выполнения, которые он требует.</span><span class="sxs-lookup"><span data-stu-id="313d2-105">Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype RequiresCapability = (Level : String, Reason : String);
```



## <a name="named-items"></a><span data-ttu-id="313d2-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="313d2-106">Named Items</span></span>

### <a name="level--string"></a><span data-ttu-id="313d2-107">Level: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="313d2-107">Level : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="313d2-108">Имя уровня возможностей среды выполнения, требуемого для вызываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="313d2-108">The name of the runtime capability level required by the callable.</span></span>
### <a name="reason--string"></a><span data-ttu-id="313d2-109">Причина: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="313d2-109">Reason : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="313d2-110">Описание причин, по которым вызываемый объект требует этой возможности среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="313d2-110">A description of why the callable requires this runtime capability.</span></span>

## <a name="remarks"></a><span data-ttu-id="313d2-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="313d2-111">Remarks</span></span>

<span data-ttu-id="313d2-112">Этот атрибут автоматически добавляется в вызываемые компилятором, если в вызываемом экземпляре уже не существует экземпляра этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="313d2-112">This attribute is automatically added to callables by the compiler, unless an instance of this attribute already exists on the callable.</span></span> <span data-ttu-id="313d2-113">Его не следует использовать, за исключением редких случаев, когда компилятор неправильно выводит требуемую возможность.</span><span class="sxs-lookup"><span data-stu-id="313d2-113">It should not be used except in rare cases where the compiler does not infer the required capability correctly.</span></span>

<span data-ttu-id="313d2-114">Ниже приведен список имен уровней возможностей в порядке увеличения возможностей или снижения ограничений.</span><span class="sxs-lookup"><span data-stu-id="313d2-114">Below is the list of capability level names, in order of increasing capabilities or decreasing restrictions:</span></span>

## `"BasicQuantumFunctionality"`

<span data-ttu-id="313d2-115">Результаты измерения не могут сравниваться на равенство.</span><span class="sxs-lookup"><span data-stu-id="313d2-115">Measurement results cannot be compared for equality.</span></span>

## `"BasicMeasurementFeedback"`

<span data-ttu-id="313d2-116">Результаты измерения можно сравнивать на равенство только в условных выражениях if-операторах в операциях.</span><span class="sxs-lookup"><span data-stu-id="313d2-116">Measurement results can be compared for equality only in if-statement conditional expressions in operations.</span></span> <span data-ttu-id="313d2-117">Блок оператора if, который зависит от результата, не может содержать инструкции SET для изменяемых переменных, объявленных за пределами блока, или операторов return.</span><span class="sxs-lookup"><span data-stu-id="313d2-117">The block of an if-statement that depends on a result cannot contain set statements for mutable variables declared outside the block, or return statements.</span></span>

## `"FullComputation"`

<span data-ttu-id="313d2-118">Нет ограничений среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="313d2-118">No runtime restrictions.</span></span> <span data-ttu-id="313d2-119">Можно выполнить любую программу Q #.</span><span class="sxs-lookup"><span data-stu-id="313d2-119">Any Q# program can be executed.</span></span>