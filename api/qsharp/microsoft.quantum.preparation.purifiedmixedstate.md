---
uid: Microsoft.Quantum.Preparation.PurifiedMixedState
title: Функция Пурифиедмикседстате
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedState
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed state.\rA \"purified mixed state\" refers to states of the form |ψ⟩ = Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |garbageᵢ⟩ specified by a vector of\rcoefficients {\U0001D45Dᵢ}. States of this form can be reduced to mixed states ρ ≔ \U0001D45Dᵢ |\U0001D456⟩⟨\U0001D456| by tracing over the \"garbage\"\rregister (that is, a mixed state that is diagonal in the computational basis).\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: 594a1d9fa674e457ab88072ade4198283b677af6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854308"
---
# <a name="purifiedmixedstate-function"></a>Функция Пурифиедмикседстате

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает операцию, которая готовит пурификатион данного смешанного состояния.
"Пурифиед смешанное состояние" относится к состояниям вида | ψ ⟩ = Σи √ PI | i ⟩ | гарбажеи ⟩, указанным вектором коэффициентов {PI}. Состояния этой формы можно сократить до смешанных состояний p ≔ PI | i ⟩ ⟨ i | Трассировка по регистру «мусора» (то есть смешанному состоянию, который является диагональным по диагонали).

Дополнительные https://arxiv.org/pdf/1805.03662.pdf?page=15 сведения см. в статье.

```qsharp
function PurifiedMixedState (targetError : Double, coefficients : Double[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a>Описание

Использует метод ПЗУ такта для представления заданной матрицы плотности, возвращая это представление в качестве операции подготовки состояния.

В частности, при наличии списка коэффициентов $N $ $ \ alpha_j $ эта функция возвращает операцию, которая использует метод ПЗУ такта для подготовки приближения $ $ \бегин{алигн} \тилде\рхо = \ sum_ {j = 0} ^ {N-1} p_j \кет{ж}\бра{ж} \енд{алигн} $ $ смешанного состояния $ $ \бегин{алигн} \рхо = \ sum_ {j = 0} ^ {N-1} \ фрак {| alpha_j |} {\ sum_k | \ alpha_k |} \кет{ж}\бра{ж}, \енд{алигн} $ $, где каждый $p _j $ является приближением к заданному коэффициенту $ \ alpha_j $ таким, что $ $ \бегин{алигн} \лефт | p_j-\фрак{| \ alpha_j |} {\ sum_k | \ alpha_k |} \ле \Фрак{\епсилон}{н} \енд{алигн} $ $ для каждого $j $.

При передаче регистра индекса и регистрации кубитса мусора изначально в состоянии $ \кет {0} \ket{00\cdots 0} возвращаемая операция готовит оба регистра в пурификатион $ \тилде \рхо $, $ $ \бегин{алигн} \ sum_ {j = 0} ^ {N-1} \скрт{p_j} \кет{ж}\кет{\текст{гарбаже} _j}, \end{align} $ $, что сброс и освобождение регистрации мусора приводит к тому, что нужная подготовка в рамках целевой ошибки $ \epsilon $.

## <a name="input"></a>Входные данные

### <a name="targeterror--double"></a>Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)

Целевая ошибка $ \епсилон $.


### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив коэффициентов $N $ с указанием вероятности базисных состояний.
Отрицательные числа $-\ alpha_j $ будут рассматриваться как положительные $ | \ alpha_j | $.



## <a name="output--mixedstatepreparation"></a>Выходные данные: [микседстатепрепаратион](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)

Операция, подготавливающая $ \тилде \рхо $ в качестве пурификатион к совместному индексу и регистрации мусора.

## <a name="example"></a>Пример

Следующий фрагмент кода подготавливает пурификатион из $3 $-кубит State $ \рхо = \ sum_ {j = 0} ^ {4} \фрак{| alpha_j |} {\ sum_k | \ alpha_k |} \кет{ж}\бра{ж} $, где $ \век\алфа = (1.0, 2,0, 3,0, 4,0, 5,0) $, а целевая ошибка — $10 ^ {-3} $:

```qsharp
let coefficients = [1.0, 2.0, 3.0, 4.0, 5.0];
let targetError = 1e-3;
let purifiedState = PurifiedMixedState(targetError, coefficients);
using (indexRegister = Qubit[purifiedState::Requirements::NIndexQubits]) {
    using (garbageRegister = Qubit[purifiedState::Requirements::NGarbageQubits]) {
        purifiedState::Prepare(LittleEndian(indexRegister), new Qubit[0], garbageRegister);
    }
}
```

## <a name="remarks"></a>Remarks

Коэффициенты, предоставляемые для этой операции, нормализованы после 1-нормы, чтобы коэффициенты, которые всегда рассматриваются, описывают допустимое распределение вероятности по категориям.

## <a name="references"></a>Ссылки

- Кодирование электронных спектра в тактовых каналах с помощью линейного T сложности Райан Баббуш, Крейг Гиднэй, Dominic W. Берри, (Nathan Виебе, Жаррод Астрид, Александру Палер, Остин Фаулер, Хартмут Невен https://arxiv.org/abs/1805.03662

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. подготовка. Пурифиедмикседстатевисдата](xref:Microsoft.Quantum.Preparation.PurifiedMixedStateWithData)