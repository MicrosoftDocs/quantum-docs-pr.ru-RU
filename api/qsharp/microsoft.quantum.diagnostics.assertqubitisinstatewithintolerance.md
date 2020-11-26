---
uid: Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance
title: Операция Ассерткубитисинстатевисинтолеранце
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitIsInStateWithinTolerance
qsharp.summary: >-
  Asserts that a qubit in the expected state.

  `expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$. The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part. The last argument defines the tolerance with which assertion is made.
ms.openlocfilehash: 1ceb7243cba93e42c67cc3655283a5d07c96863e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202215"
---
# <a name="assertqubitisinstatewithintolerance-operation"></a><span data-ttu-id="dd097-102">Операция Ассерткубитисинстатевисинтолеранце</span><span class="sxs-lookup"><span data-stu-id="dd097-102">AssertQubitIsInStateWithinTolerance operation</span></span>

<span data-ttu-id="dd097-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="dd097-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="dd097-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="dd097-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="dd097-105">Утверждает, что кубит находится в ожидаемом состоянии.</span><span class="sxs-lookup"><span data-stu-id="dd097-105">Asserts that a qubit in the expected state.</span></span>

<span data-ttu-id="dd097-106">`expected` представляет сложный вектор, $ \кет{\пси} = \бегин{бматрикс}а & б\енд {бматрикс} ^ {\Масрм{т}} $.</span><span class="sxs-lookup"><span data-stu-id="dd097-106">`expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$.</span></span>
<span data-ttu-id="dd097-107">Первый элемент кортежей, представляющий каждый из $a $, $b $ является реальной частью комплексного числа, а второй — мнимой частью.</span><span class="sxs-lookup"><span data-stu-id="dd097-107">The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part.</span></span>
<span data-ttu-id="dd097-108">Последний аргумент определяет допуск, с которым выполняется утверждение.</span><span class="sxs-lookup"><span data-stu-id="dd097-108">The last argument defines the tolerance with which assertion is made.</span></span>

```qsharp
operation AssertQubitIsInStateWithinTolerance (expected : (Microsoft.Quantum.Math.Complex, Microsoft.Quantum.Math.Complex), register : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="dd097-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="dd097-109">Input</span></span>

### <a name="expected--complexcomplex"></a><span data-ttu-id="dd097-110">ожидалось: ([сложное](xref:Microsoft.Quantum.Math.Complex),[сложное](xref:Microsoft.Quantum.Math.Complex))</span><span class="sxs-lookup"><span data-stu-id="dd097-110">expected : ([Complex](xref:Microsoft.Quantum.Math.Complex),[Complex](xref:Microsoft.Quantum.Math.Complex))</span></span>

<span data-ttu-id="dd097-111">Ожидаемые сложные амплитуды для $ \кет {0} $ и $ \кет {1} $ соответственно.</span><span class="sxs-lookup"><span data-stu-id="dd097-111">Expected complex amplitudes for $\ket{0}$ and $\ket{1}$, respectively.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="dd097-112">Регистрация: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dd097-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dd097-113">Кубит, состояние которого должно быть утверждено.</span><span class="sxs-lookup"><span data-stu-id="dd097-113">Qubit whose state is to be asserted.</span></span> <span data-ttu-id="dd097-114">Обратите внимание, что предполагается, что кубит отделяемых из других выделенных Кубитс, а не запутанными.</span><span class="sxs-lookup"><span data-stu-id="dd097-114">Note that this qubit is assumed to be separable from other allocated qubits, and not entangled.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="dd097-115">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="dd097-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="dd097-116">Аддитивная погрешность, с которой действительные амплитуды могут отклоняться от ожидаемого.</span><span class="sxs-lookup"><span data-stu-id="dd097-116">Additive tolerance by which actual amplitudes are allowed to deviate from expected.</span></span>
<span data-ttu-id="dd097-117">Дополнительные сведения см. в примечаниях ниже.</span><span class="sxs-lookup"><span data-stu-id="dd097-117">See remarks below for details.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dd097-118">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dd097-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="dd097-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd097-119">Remarks</span></span>

<span data-ttu-id="dd097-120">Следующий код Масематика можно использовать для проверки выражений для MI, MX, My, MZ:</span><span class="sxs-lookup"><span data-stu-id="dd097-120">The following Mathematica code can be used to verify expressions for mi, mx, my, mz:</span></span>

```mathematica
{Id, X, Y, Z} = Table[PauliMatrix[k], {k, 0, 3}];
st = {{ reA + I imA }, { reB + I imB} };
M = st . ConjugateTranspose[st];
mx = Tr[M.X] // ComplexExpand;
my = Tr[M.Y] // ComplexExpand;
mz = Tr[M.Z] // ComplexExpand;
mi = Tr[M.Id] // ComplexExpand;
2 m == Id mi + X mx + Z mz + Y my // ComplexExpand // Simplify
```

<span data-ttu-id="dd097-121">Допуск — это $L \_ {\инфти} $ Distance между трехмерным реальным вектором (x ₂, x ₃, x ₄), определяемый $ \лангле\пси | \пси\рангле = x \_ 1 I + x \_ 2 x + x \_ 3 Y + x \_ 4 Z $ и вещественный вектор (y ₂, y ₃, Y ₄), определенный p = y ₁ I + y ₂ x + y ₃ Y + y ₄ Z, где p — это матрица плотности, соответствующая состоянию регистра.</span><span class="sxs-lookup"><span data-stu-id="dd097-121">The tolerance is the $L\_{\infty}$ distance between 3 dimensional real vector (x₂,x₃,x₄) defined by $\langle\psi|\psi\rangle = x\_1 I + x\_2 X + x\_3 Y + x\_4 Z$ and real vector (y₂,y₃,y₄) defined by ρ = y₁I + y₂X + y₃Y + y₄Z where ρ is the density matrix corresponding to the state of the register.</span></span>
<span data-ttu-id="dd097-122">Это справедливо только в случае предположения, что TR (p) и TR (| ψ ⟩ ⟨ ψ |) равны 1 (например, x ₁ = 1/2, y ₁ = 1/2).</span><span class="sxs-lookup"><span data-stu-id="dd097-122">This is only true under the assumption that Tr(ρ) and Tr(|ψ⟩⟨ψ|) are both 1 (e.g. x₁ = 1/2, y₁ = 1/2).</span></span>
<span data-ttu-id="dd097-123">Если это не так, функция утверждает, что l ∞ расстояние между (x ₂-x ₁, x ₃-x ₁, x ₄-x ₁, x ₄ + x ₁) и (y ₂-y ₁, y ₃-y ₁, y ₄-y ₁, y ₄ + y ₁) меньше, чем параметр допуска.</span><span class="sxs-lookup"><span data-stu-id="dd097-123">If this is not the case, the function asserts that l∞ distance between (x₂-x₁,x₃-x₁,x₄-x₁,x₄+x₁) and (y₂-y₁,y₃-y₁,y₄-y₁,y₄+y₁) is less than the tolerance parameter.</span></span>