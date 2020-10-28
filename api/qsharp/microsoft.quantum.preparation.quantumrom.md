---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: Функция Куантумром
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 8ba5c6fab4abcfaee7233df9535f22eea5f68c28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732624"
---
# <a name="quantumrom-function"></a><span data-ttu-id="61427-102">Функция Куантумром</span><span class="sxs-lookup"><span data-stu-id="61427-102">QuantumROM function</span></span>

<span data-ttu-id="61427-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="61427-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="61427-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="61427-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="61427-105">Использует методику такта для представления заданной матрицы плотности.</span><span class="sxs-lookup"><span data-stu-id="61427-105">Uses the Quantum ROM technique to represent a given density matrix.</span></span>

<span data-ttu-id="61427-106">Учитывая список коэффициентов $N $ alpha_j $, он возвращает единую $U $, которая использует методику такта для подготовки приближения $ \тилде\рхо\ sum_ {j = 0} ^ {N-1} p_j \кет{ж}\бра{ж} $ пурификатион матрицы плотности $ \рхо = \ sum_ {j = 0} ^ {N-1} \фрак{| alpha_j |} {\ sum_k | \ alpha_k |} \кет{ж}\бра{ж} $.</span><span class="sxs-lookup"><span data-stu-id="61427-106">Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$.</span></span> <span data-ttu-id="61427-107">В этом приближении ошибка $ \епсилон $ заключается в том, что $ | p_j-\фрак{| alpha_j |} {\ sum_k | \ alpha_k |} | \ле \епсилон/N $ and $ \| \тилде\рхо-\рхо \| \ле \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="61427-107">In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$.</span></span> <span data-ttu-id="61427-108">Иными словами, $ $ \бегин{алигн} У\кет {0} ^ {\лцеил\ Log_2 н\рцеил} \ Сисакет {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \скрт{p_j} \кет{ж}\кет{\текст{гарбаже} _j}.</span><span class="sxs-lookup"><span data-stu-id="61427-108">In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}.</span></span>
<span data-ttu-id="61427-109">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="61427-109">\end{align} $$</span></span>

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a><span data-ttu-id="61427-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="61427-110">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="61427-111">Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="61427-111">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="61427-112">Целевая ошибка $ \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="61427-112">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="61427-113">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="61427-113">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="61427-114">Массив коэффициентов $N $ с указанием вероятности базисных состояний.</span><span class="sxs-lookup"><span data-stu-id="61427-114">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="61427-115">Отрицательные числа $-\ alpha_j $ будут рассматриваться как положительные $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="61427-115">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--intintintdoublelittleendianqubit--unit-adj--ctl"></a><span data-ttu-id="61427-116">Выходные данные: ([(int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))[, Double](xref:microsoft.quantum.lang-ref.double), ([литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = [>ная](xref:microsoft.quantum.lang-ref.unit) Нагода + CTL)</span><span class="sxs-lookup"><span data-stu-id="61427-116">Output : (([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double),([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span></span>

## <a name="first-parameter"></a><span data-ttu-id="61427-117">Первый параметр</span><span class="sxs-lookup"><span data-stu-id="61427-117">First parameter</span></span>

<span data-ttu-id="61427-118">Кортеж, `(x,(y,z))` где `x = y + z` — Общее число выделенных Кубитс, `y` — число Кубитс для `LittleEndian` регистра, а `z` — число Кубитс мусора.</span><span class="sxs-lookup"><span data-stu-id="61427-118">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="61427-119">Второй параметр</span><span class="sxs-lookup"><span data-stu-id="61427-119">Second parameter</span></span>

<span data-ttu-id="61427-120">Один из норм $ \ sum_j | \ alpha_j | $ массива коэффициента.</span><span class="sxs-lookup"><span data-stu-id="61427-120">The one-norm $\sum_j |\alpha_j|$ of the coefficient array.</span></span>

## <a name="third-parameter"></a><span data-ttu-id="61427-121">Третий параметр</span><span class="sxs-lookup"><span data-stu-id="61427-121">Third parameter</span></span>

<span data-ttu-id="61427-122">Единая $U $.</span><span class="sxs-lookup"><span data-stu-id="61427-122">The unitary $U$.</span></span>

## <a name="references"></a><span data-ttu-id="61427-123">Ссылки</span><span class="sxs-lookup"><span data-stu-id="61427-123">References</span></span>

- <span data-ttu-id="61427-124">Кодирование электронных спектра в тактовых каналах с помощью линейного T сложности Райан Баббуш, Крейг Гиднэй, Dominic W. Берри, (Nathan Виебе, Жаррод Астрид, Александру Палер, Остин Фаулер, Хартмут Невен https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="61427-124">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>