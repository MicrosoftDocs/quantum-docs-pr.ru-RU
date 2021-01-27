---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Определяемый пользователем тип Комплексполар
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 174e75b82a3ee740cd4d07e5bcd091de65bbc6b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847352"
---
# <a name="complexpolar-user-defined-type"></a><span data-ttu-id="5caae-102">Определяемый пользователем тип Комплексполар</span><span class="sxs-lookup"><span data-stu-id="5caae-102">ComplexPolar user defined type</span></span>

<span data-ttu-id="5caae-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="5caae-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="5caae-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5caae-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5caae-105">Представляет комплексное число в полярной форме.</span><span class="sxs-lookup"><span data-stu-id="5caae-105">Represents a complex number in polar form.</span></span>

<span data-ttu-id="5caae-106">Полярное представление комплексного числа имеет $c = r e ^ {i t} $.</span><span class="sxs-lookup"><span data-stu-id="5caae-106">The polar representation of a complex number is $c=r e^{i t}$.</span></span>

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a><span data-ttu-id="5caae-107">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="5caae-107">Named Items</span></span>

### <a name="magnitude--double"></a><span data-ttu-id="5caae-108">Величина: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5caae-108">Magnitude : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5caae-109">Абсолютное значение $r \же $0 из $c $.</span><span class="sxs-lookup"><span data-stu-id="5caae-109">The absolute value $r \ge 0$ of $c$.</span></span>
### <a name="argument--double"></a><span data-ttu-id="5caae-110">Аргумент: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5caae-110">Argument : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5caae-111">Фаза $t \ин \масбб R $ of $c $.</span><span class="sxs-lookup"><span data-stu-id="5caae-111">The phase $t \in \mathbb R$ of $c$.</span></span>