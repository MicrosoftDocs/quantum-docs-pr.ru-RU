---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEXY
title: Операция Оптимизедбекси
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEXY
qsharp.summary: A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$. That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$
ms.openlocfilehash: 28a7c7877a3d48fd5ba50384d7996017e7cdb14f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98837251"
---
# <a name="optimizedbexy-operation"></a><span data-ttu-id="42303-102">Операция Оптимизедбекси</span><span class="sxs-lookup"><span data-stu-id="42303-102">OptimizedBEXY operation</span></span>

<span data-ttu-id="42303-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="42303-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="42303-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="42303-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="42303-105">Единая $U $, которая применяет строку Паули в $ (X ^ {z + 1} \_ Корр. {z} \_ p) z \_ {p-1}... Z_0 $0.. p $ включено в индекс $z \ин \{ 0, 1 \} $ и $p $.</span><span class="sxs-lookup"><span data-stu-id="42303-105">A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$.</span></span> <span data-ttu-id="42303-106">Т. е. $ $ \бегин{алигн} У\кет {z} \ Сисакет {p} \ Сисакет {\ PSI} = \кет{з}\кет{п} (X ^ {z + 1} \_ Корр. {z} \_ p) z \_ {p-1}... Z_0 \кет{\пси} \енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="42303-106">That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$</span></span>

```qsharp
operation OptimizedBEXY (pauliBasis : Qubit, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="42303-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="42303-107">Input</span></span>

### <a name="paulibasis--qubit"></a><span data-ttu-id="42303-108">Паулибасис: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="42303-108">pauliBasis : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="42303-109">Если кубит находится в состоянии $ \кет {0} $, применяется $X $.</span><span class="sxs-lookup"><span data-stu-id="42303-109">When this qubit is in state $\ket{0}$, $X$ is applied.</span></span> <span data-ttu-id="42303-110">Когда он находится в состоянии $ \кет {1} $, применяется $Y $.</span><span class="sxs-lookup"><span data-stu-id="42303-110">When it is in state $\ket{1}$, $Y$ is applied.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="42303-111">Индексрегистер: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="42303-111">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="42303-112">Состояние $ \кет{п} $ этого регистра определяет кубит, к которому применяется $X $ или $Y $ $.</span><span class="sxs-lookup"><span data-stu-id="42303-112">The state $\ket{p}$ of this register determines the qubit on which $X$ or $Y$ is applied.</span></span>


### <a name="targetregister--qubit"></a><span data-ttu-id="42303-113">Таржетрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="42303-113">targetRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="42303-114">Регистрация Кубитс, к которой применяются операторы Паули.</span><span class="sxs-lookup"><span data-stu-id="42303-114">Register of qubits on which the Pauli operators are applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="42303-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="42303-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="42303-116">Ссылки</span><span class="sxs-lookup"><span data-stu-id="42303-116">References</span></span>

- <span data-ttu-id="42303-117">Кодирование электронных спектра в тактовых каналах с помощью линейного T сложности Райан Баббуш, Крейг Гиднэй, Dominic W. Берри, (Nathan Виебе, Жаррод Астрид, Александру Палер, Остин Фаулер, Хартмут Невен https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="42303-117">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>