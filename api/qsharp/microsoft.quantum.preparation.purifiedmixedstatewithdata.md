---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateWithData
title: Функция Пурифиедмикседстатевисдата
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateWithData
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed\rstate, entangled with a register representing a given collection of data.\rA \"purified mixed state with data\" refers to a state of the form Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |\U0001D465ᵢ⟩ |garbageᵢ⟩,\rwhere each \U0001D465ᵢ is a bitstring encoding additional data associated with the register |\U0001D456⟩.\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: fc7bf8e6157af079ae4233ef45e67ce8ddfb8fe3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854281"
---
# <a name="purifiedmixedstatewithdata-function"></a>Функция Пурифиедмикседстатевисдата

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает операцию, которая готовит пурификатион данного смешанного состояния, запутанными с регистром, представляющим данную коллекцию данных.
"Пурифиед смешанное состояние с данными" относится к состоянию вида Σи √ PI | i ⟩ | XI ⟩ | гарбажеи ⟩, где каждое значение XI является битстринг кодировкой дополнительных данных, связанных с регистрацией | i ⟩.

Дополнительные https://arxiv.org/pdf/1805.03662.pdf?page=15 сведения см. в статье.

```qsharp
function PurifiedMixedStateWithData (targetError : Double, coefficients : (Double, Bool[])[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a>Описание

Использует метод ПЗУ такта для представления заданной матрицы плотности, возвращая это представление в качестве операции подготовки состояния.

В частности, при наличии списка коэффициентов "$N $" $ \ alpha_j $ и битстринг $ \век{КС}_j $, связанных с каждым из них, эта функция возвращает операцию, которая использует метод ПЗУ такта для подготовки приближения $ $ \бегин{алигн} \тилде\рхо = \сум_{j = 0} ^ {N-1} p_j \кет{ж}\бра{ж} \отимес \кет{\век{КС} _j} \bra{\vec{x}_j} \end{align} $ $ из смешанного состояния $ $ \begin{align} \rho = \sum_{j = 0} ^ {N-1} \ frac {| alpha_j |} {\ sum_k | \ alpha_k |} \кет{ж}\бра{ж} \отимес \кет{\век{КС} _j} \бра{\век{КС} _j}, \енд{алигн} $ $ где каждый $p _j $ является приближением к заданному коэффициенту $ \ alpha_j $ таким, что $ $ \бегин{алигн} \лефт | p_j-\фрак{| \ alpha_j |} {\ sum_k | \ alpha_k |} \ле \Фрак{\епсилон}{н} \енд{алигн} $ $ для каждого $j $.

Когда передается регистр индекса и регистр Кубитс мусора, первоначально находится в состоянии $ \кет {0} \ket{00\cdots 0}, возвращаемая операция готовит обе регистрации в пурификатион $ \тилде \рхо $, $ $ \бегин{алигн} \ sum_ {j = 0} ^ {N-1} \скрт{p_j} \кет{ж} \кет{\век{кс} _j} \кет{\текст{гарбаже} _j}, \end{align} $ $ например, при сбросе и отмене выделения для регистрации мусора нужная подготовка в рамках целевой ошибки $ \epsilon $.

## <a name="input"></a>Входные данные

### <a name="targeterror--double"></a>Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)

Целевая ошибка $ \епсилон $.


### <a name="coefficients--doublebool"></a>коэффициенты: ([Double](xref:microsoft.quantum.lang-ref.double),[bool](xref:microsoft.quantum.lang-ref.bool)[]) []

Массив коэффициентов $N $ с указанием вероятности базисных состояний, а также битстринг $ \век{КС} _j $, связанный с каждым подмножеством.
Отрицательные числа $-\ alpha_j $ будут рассматриваться как положительные $ | \ alpha_j | $.



## <a name="output--mixedstatepreparation"></a>Выходные данные: [микседстатепрепаратион](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)

Операция, подготавливающая $ \тилде \рхо $ в качестве пурификатион к совместному индексу и регистрации мусора.

## <a name="remarks"></a>Remarks

Коэффициенты, предоставляемые для этой операции, нормализованы после 1-нормы, чтобы коэффициенты, которые всегда рассматриваются, описывают допустимое распределение вероятности по категориям.

## <a name="references"></a>Ссылки

- Кодирование электронных спектра в тактовых каналах с помощью линейного T сложности Райан Баббуш, Крейг Гиднэй, Dominic W. Берри, (Nathan Виебе, Жаррод Астрид, Александру Палер, Остин Фаулер, Хартмут Невен https://arxiv.org/abs/1805.03662

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. подготовка. Пурифиедмикседстате](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)