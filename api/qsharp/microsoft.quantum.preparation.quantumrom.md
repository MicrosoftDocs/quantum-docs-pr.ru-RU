---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: Функция Куантумром
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  > [!WARNING]

  > QuantumROM has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.


  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 1ee805fb2ea02121daaab7fc3eb5dbbcb134b470
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229891"
---
# <a name="quantumrom-function"></a><span data-ttu-id="7dabf-102">Функция Куантумром</span><span class="sxs-lookup"><span data-stu-id="7dabf-102">QuantumROM function</span></span>

<span data-ttu-id="7dabf-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="7dabf-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="7dabf-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7dabf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="7dabf-105">Куантумром является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="7dabf-105">QuantumROM has been deprecated.</span></span> <span data-ttu-id="7dabf-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Preparation.PurifiedMixedState>.</span><span class="sxs-lookup"><span data-stu-id="7dabf-106">Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.</span></span>

<span data-ttu-id="7dabf-107">Использует методику такта для представления заданной матрицы плотности.</span><span class="sxs-lookup"><span data-stu-id="7dabf-107">Uses the Quantum ROM technique to represent a given density matrix.</span></span>

<span data-ttu-id="7dabf-108">Учитывая список коэффициентов $N $ alpha_j $, он возвращает единую $U $, которая использует методику такта для подготовки приближения $ \тилде\рхо\ sum_ {j = 0} ^ {N-1} p_j \кет{ж}\бра{ж} $ пурификатион матрицы плотности $ \рхо = \ sum_ {j = 0} ^ {N-1} \фрак{| alpha_j |} {\ sum_k | \ alpha_k |} \кет{ж}\бра{ж} $.</span><span class="sxs-lookup"><span data-stu-id="7dabf-108">Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$.</span></span> <span data-ttu-id="7dabf-109">В этом приближении ошибка $ \епсилон $ заключается в том, что $ | p_j-\фрак{| alpha_j |} {\ sum_k | \ alpha_k |} | \ле \епсилон/N $ and $ \| \тилде\рхо-\рхо \| \ле \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="7dabf-109">In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$.</span></span> <span data-ttu-id="7dabf-110">Иными словами, $ $ \бегин{алигн} У\кет {0} ^ {\лцеил\ Log_2 н\рцеил} \ Сисакет {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \скрт{p_j} \кет{ж}\кет{\текст{гарбаже} _j}.</span><span class="sxs-lookup"><span data-stu-id="7dabf-110">In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}.</span></span>
<span data-ttu-id="7dabf-111">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="7dabf-111">\end{align} $$</span></span>

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a><span data-ttu-id="7dabf-112">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7dabf-112">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="7dabf-113">Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7dabf-113">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7dabf-114">Целевая ошибка $ \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="7dabf-114">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="7dabf-115">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="7dabf-115">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="7dabf-116">Массив коэффициентов $N $ с указанием вероятности базисных состояний.</span><span class="sxs-lookup"><span data-stu-id="7dabf-116">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="7dabf-117">Отрицательные числа $-\ alpha_j $ будут рассматриваться как положительные $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="7dabf-117">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--intintintdoublelittleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="7dabf-118">Выходные данные: (([int](xref:microsoft.quantum.lang-ref.int),[(int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))[, Double](xref:microsoft.quantum.lang-ref.double), ([Литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "прилагательные" и "CTL")</span><span class="sxs-lookup"><span data-stu-id="7dabf-118">Output : (([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double),([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

## <a name="first-parameter"></a><span data-ttu-id="7dabf-119">Первый параметр</span><span class="sxs-lookup"><span data-stu-id="7dabf-119">First parameter</span></span>

<span data-ttu-id="7dabf-120">Кортеж, `(x,(y,z))` где `x = y + z` — Общее число выделенных Кубитс, `y` — число Кубитс для `LittleEndian` регистра, а `z` — число Кубитс мусора.</span><span class="sxs-lookup"><span data-stu-id="7dabf-120">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="7dabf-121">Второй параметр</span><span class="sxs-lookup"><span data-stu-id="7dabf-121">Second parameter</span></span>

<span data-ttu-id="7dabf-122">Один из норм $ \ sum_j | \ alpha_j | $ массива коэффициента.</span><span class="sxs-lookup"><span data-stu-id="7dabf-122">The one-norm $\sum_j |\alpha_j|$ of the coefficient array.</span></span>

## <a name="third-parameter"></a><span data-ttu-id="7dabf-123">Третий параметр</span><span class="sxs-lookup"><span data-stu-id="7dabf-123">Third parameter</span></span>

<span data-ttu-id="7dabf-124">Единая $U $.</span><span class="sxs-lookup"><span data-stu-id="7dabf-124">The unitary $U$.</span></span>

## <a name="references"></a><span data-ttu-id="7dabf-125">Ссылки</span><span class="sxs-lookup"><span data-stu-id="7dabf-125">References</span></span>

- <span data-ttu-id="7dabf-126">Кодирование электронных спектра в тактовых каналах с помощью линейного T сложности Райан Баббуш, Крейг Гиднэй, Dominic W. Берри, (Nathan Виебе, Жаррод Астрид, Александру Палер, Остин Фаулер, Хартмут Невен https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="7dabf-126">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>