---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: Функция Куантумром
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  > [!WARNING]

  > QuantumROM has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.


  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 64ed9aed7c9d9a4a689c5926f3cd085a2521c4db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856821"
---
# <a name="quantumrom-function"></a><span data-ttu-id="a2d10-102">Функция Куантумром</span><span class="sxs-lookup"><span data-stu-id="a2d10-102">QuantumROM function</span></span>

<span data-ttu-id="a2d10-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="a2d10-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="a2d10-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a2d10-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="a2d10-105">Куантумром является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="a2d10-105">QuantumROM has been deprecated.</span></span> <span data-ttu-id="a2d10-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Preparation.PurifiedMixedState>.</span><span class="sxs-lookup"><span data-stu-id="a2d10-106">Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.</span></span>

<span data-ttu-id="a2d10-107">Использует методику такта для представления заданной матрицы плотности.</span><span class="sxs-lookup"><span data-stu-id="a2d10-107">Uses the Quantum ROM technique to represent a given density matrix.</span></span>

<span data-ttu-id="a2d10-108">Учитывая список коэффициентов $N $ alpha_j $, он возвращает единую $U $, которая использует методику такта для подготовки приближения $ \тилде\рхо\ sum_ {j = 0} ^ {N-1} p_j \кет{ж}\бра{ж} $ пурификатион матрицы плотности $ \рхо = \ sum_ {j = 0} ^ {N-1} \фрак{| alpha_j |} {\ sum_k | \ alpha_k |} \кет{ж}\бра{ж} $.</span><span class="sxs-lookup"><span data-stu-id="a2d10-108">Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$.</span></span> <span data-ttu-id="a2d10-109">В этом приближении ошибка $ \епсилон $ заключается в том, что $ | p_j-\фрак{| alpha_j |} {\ sum_k | \ alpha_k |} | \ле \епсилон/N $ and $ \| \тилде\рхо-\рхо \| \ле \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="a2d10-109">In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$.</span></span> <span data-ttu-id="a2d10-110">Иными словами, $ $ \бегин{алигн} У\кет {0} ^ {\лцеил\ Log_2 н\рцеил} \ Сисакет {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \скрт{p_j} \кет{ж}\кет{\текст{гарбаже} _j}.</span><span class="sxs-lookup"><span data-stu-id="a2d10-110">In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}.</span></span>
<span data-ttu-id="a2d10-111">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="a2d10-111">\end{align} $$</span></span>

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a><span data-ttu-id="a2d10-112">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a2d10-112">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="a2d10-113">Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a2d10-113">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a2d10-114">Целевая ошибка $ \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="a2d10-114">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="a2d10-115">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a2d10-115">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a2d10-116">Массив коэффициентов $N $ с указанием вероятности базисных состояний.</span><span class="sxs-lookup"><span data-stu-id="a2d10-116">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="a2d10-117">Отрицательные числа $-\ alpha_j $ будут рассматриваться как положительные $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="a2d10-117">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--intintintdoublelittleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="a2d10-118">Выходные данные: (([int](xref:microsoft.quantum.lang-ref.int),[(int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))[, Double](xref:microsoft.quantum.lang-ref.double), ([Литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "прилагательные" и "CTL")</span><span class="sxs-lookup"><span data-stu-id="a2d10-118">Output : (([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double),([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

## <a name="first-parameter"></a><span data-ttu-id="a2d10-119">Первый параметр</span><span class="sxs-lookup"><span data-stu-id="a2d10-119">First parameter</span></span>

<span data-ttu-id="a2d10-120">Кортеж, `(x,(y,z))` где `x = y + z` — Общее число выделенных Кубитс, `y` — число Кубитс для `LittleEndian` регистра, а `z` — число Кубитс мусора.</span><span class="sxs-lookup"><span data-stu-id="a2d10-120">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="a2d10-121">Второй параметр</span><span class="sxs-lookup"><span data-stu-id="a2d10-121">Second parameter</span></span>

<span data-ttu-id="a2d10-122">Один из норм $ \ sum_j | \ alpha_j | $ массива коэффициента.</span><span class="sxs-lookup"><span data-stu-id="a2d10-122">The one-norm $\sum_j |\alpha_j|$ of the coefficient array.</span></span>

## <a name="third-parameter"></a><span data-ttu-id="a2d10-123">Третий параметр</span><span class="sxs-lookup"><span data-stu-id="a2d10-123">Third parameter</span></span>

<span data-ttu-id="a2d10-124">Единая $U $.</span><span class="sxs-lookup"><span data-stu-id="a2d10-124">The unitary $U$.</span></span>

## <a name="example"></a><span data-ttu-id="a2d10-125">Пример</span><span class="sxs-lookup"><span data-stu-id="a2d10-125">Example</span></span>

<span data-ttu-id="a2d10-126">Следующий фрагмент кода подготавливает пурификатион из $3 $-кубит State $ \рхо = \ sum_ {j = 0} ^ {4} \фрак{| alpha_j |} {\ sum_k | \ alpha_k |} \кет{ж}\бра{ж} $, где $ \век\алфа = (1.0, 2.0, 3.0, 4.0, 5.0) $, а ошибка — `1e-3` ;</span><span class="sxs-lookup"><span data-stu-id="a2d10-126">The following code snippet prepares an purification of the $3$-qubit state $\rho=\sum_{j=0}^{4}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$, where $\vec\alpha=(1.0,2.0,3.0,4.0,5.0)$, and the error is `1e-3`;</span></span>

```qsharp
let coefficients = [1.0,2.0,3.0,4.0,5.0];
let targetError = 1e-3;
let ((nTotalQubits, (nIndexQubits, nGarbageQubits)), oneNorm, op) = QuantumROM(targetError, coefficients);
using (indexRegister = Qubit[nIndexQubits]) {
    using (garbageRegister = Qubit[nGarbageQubits]) {
        op(LittleEndian(indexRegister), garbageRegister);
    }
}
```

## <a name="references"></a><span data-ttu-id="a2d10-127">Ссылки</span><span class="sxs-lookup"><span data-stu-id="a2d10-127">References</span></span>

- <span data-ttu-id="a2d10-128">Кодирование электронных спектра в тактовых каналах с помощью линейного T сложности Райан Баббуш, Крейг Гиднэй, Dominic W. Берри, (Nathan Виебе, Жаррод Астрид, Александру Палер, Остин Фаулер, Хартмут Невен https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="a2d10-128">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>