---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Определяемый пользователем тип Комплексполар
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: a4f3a7b6ffa73271d7ac9674d8c718f6f09c0291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210987"
---
# <a name="complexpolar-user-defined-type"></a><span data-ttu-id="e8b3f-102">Определяемый пользователем тип Комплексполар</span><span class="sxs-lookup"><span data-stu-id="e8b3f-102">ComplexPolar user defined type</span></span>

<span data-ttu-id="e8b3f-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="e8b3f-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="e8b3f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8b3f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8b3f-105">Представляет комплексное число в полярной форме.</span><span class="sxs-lookup"><span data-stu-id="e8b3f-105">Represents a complex number in polar form.</span></span>

<span data-ttu-id="e8b3f-106">Полярное представление комплексного числа имеет $c = r e ^ {i t} $.</span><span class="sxs-lookup"><span data-stu-id="e8b3f-106">The polar representation of a complex number is $c=r e^{i t}$.</span></span>

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a><span data-ttu-id="e8b3f-107">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="e8b3f-107">Named Items</span></span>

### <a name="magnitude--double"></a><span data-ttu-id="e8b3f-108">Величина: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e8b3f-108">Magnitude : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e8b3f-109">Абсолютное значение $r \же $0 из $c $.</span><span class="sxs-lookup"><span data-stu-id="e8b3f-109">The absolute value $r \ge 0$ of $c$.</span></span>
### <a name="argument--double"></a><span data-ttu-id="e8b3f-110">Аргумент: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e8b3f-110">Argument : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e8b3f-111">Фаза $t \ин \масбб R $ of $c $.</span><span class="sxs-lookup"><span data-stu-id="e8b3f-111">The phase $t \in \mathbb R$ of $c$.</span></span>