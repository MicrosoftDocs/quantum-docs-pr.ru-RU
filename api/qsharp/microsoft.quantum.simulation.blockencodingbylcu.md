---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: Функция Блоккенкодингбилку
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 04738aa54ce8b719b05954824e3553388a995df0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733712"
---
# <a name="blockencodingbylcu-function"></a>Функция Блоккенкодингбилку

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакеты [](https://nuget.org/packages/)


Кодирует интересующий оператор в `BlockEncoding` .

Создается `BlockEncoding` единая $U = П\кдот В\кдот P ^ \дагжер $, которая кодирует некоторый оператор $H = \ sum_ {j} | \ alpha_j | U_j $, представляющая собой линейное сочетание унитариес. Как правило, $P $ является подготовкой состояния, таким, что $P \кет {0} \_ a = \ sum_j \скрт{\ alpha_j/ \| \век\алфа \| \_ 2} \кет{ж} \_ a $ и $V = \ sum_ {j} \кет{ж}\бра{ж} \_ а\отимес U_j $.

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="statepreparation--t--unit-adj--ctl"></a>Статепрепаратион: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL

Единое $P $, которое готовит конечное состояние.


### <a name="selector--ts--unit-adj--ctl"></a>селектор: ('T) [=>ная](xref:microsoft.quantum.lang-ref.unit) расгода и список доверия

Единое $V $, которое кодирует компонент унитариес $H $.



## <a name="output--ts--unit-adj--ctl"></a>Выходные данные: ('T) [=>ная](xref:microsoft.quantum.lang-ref.unit) расгода и список доверия

Единая $U $ взаимодействует с регистрами `a` и `s` кодирует $H $ и соответствует $U ^ \Дагжер = U $.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="s"></a>Возникл



## <a name="remarks"></a>Remarks

Эта `BlockEncoding` Реализация предоставляет ей свойства `BlockEncodingReflection` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Блоккенкодинг](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. тактов. моделирование. Блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)