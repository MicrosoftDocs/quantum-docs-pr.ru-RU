---
uid: Microsoft.Quantum.Preparation.BlochSphereCoordinates
title: Функция Блочсферекурдинатес
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: BlochSphereCoordinates
qsharp.summary: >-
  Computes the Bloch sphere coordinates for a single-qubit state.

  Given two complex numbers $a0, a1$ that represent the qubit state, computes coordinates on the Bloch sphere such that $a0 \ket{0} + a1 \ket{1} = r e^{it}(e^{-i \phi /2}\cos{(\theta/2)}\ket{0}+e^{i \phi /2}\sin{(\theta/2)}\ket{1})$.
ms.openlocfilehash: 6614b78c8e64c205cc94052cc64dd957814ab3d0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733264"
---
# <a name="blochspherecoordinates-function"></a><span data-ttu-id="45e51-102">Функция Блочсферекурдинатес</span><span class="sxs-lookup"><span data-stu-id="45e51-102">BlochSphereCoordinates function</span></span>

<span data-ttu-id="45e51-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="45e51-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="45e51-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="45e51-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="45e51-105">Выполняет вычисление координат БЛОЧ-сферы для одного кубит состояния.</span><span class="sxs-lookup"><span data-stu-id="45e51-105">Computes the Bloch sphere coordinates for a single-qubit state.</span></span>

<span data-ttu-id="45e51-106">Учитывая два комплексных числа $a 0, a1 $, которые представляют состояние кубит, рассчитывает координаты в блочной сфере, что $a 0 \кет {0} + a1 \кет {1} = r e ^ {IT} (e ^ {-i \фи/2}\cos{(\ тета/2)} \кет {0} + e ^ {i \фи/2}\sin{(\ тета/2)} \кет {1} ) $.</span><span class="sxs-lookup"><span data-stu-id="45e51-106">Given two complex numbers $a0, a1$ that represent the qubit state, computes coordinates on the Bloch sphere such that $a0 \ket{0} + a1 \ket{1} = r e^{it}(e^{-i \phi /2}\cos{(\theta/2)}\ket{0}+e^{i \phi /2}\sin{(\theta/2)}\ket{1})$.</span></span>

```qsharp
function BlochSphereCoordinates (a0 : Microsoft.Quantum.Math.ComplexPolar, a1 : Microsoft.Quantum.Math.ComplexPolar) : (Microsoft.Quantum.Math.ComplexPolar, Double, Double)
```


## <a name="input"></a><span data-ttu-id="45e51-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="45e51-107">Input</span></span>

### <a name="a0--complexpolar"></a><span data-ttu-id="45e51-108">a0: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="45e51-108">a0 : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="45e51-109">Сложный коэффициент состояния $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="45e51-109">Complex coefficient of state $\ket{0}$.</span></span>


### <a name="a1--complexpolar"></a><span data-ttu-id="45e51-110">a1: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="45e51-110">a1 : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="45e51-111">Сложный коэффициент состояния $ \кет {1} $.</span><span class="sxs-lookup"><span data-stu-id="45e51-111">Complex coefficient of state $\ket{1}$.</span></span>



## <a name="output--complexpolardoubledouble"></a><span data-ttu-id="45e51-112">Выходные данные: ([комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar),[Double](xref:microsoft.quantum.lang-ref.double),[double](xref:microsoft.quantum.lang-ref.double))</span><span class="sxs-lookup"><span data-stu-id="45e51-112">Output : ([ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar),[Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))</span></span>

<span data-ttu-id="45e51-113">Кортеж, содержащий `(ComplexPolar(r, t), phi, theta)` .</span><span class="sxs-lookup"><span data-stu-id="45e51-113">A tuple containing `(ComplexPolar(r, t), phi, theta)`.</span></span>