---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: Функция Блоккенкодингбилку
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 254ace01750f94e6c871de9b62f1342000bc84ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229551"
---
# <a name="blockencodingbylcu-function"></a>Функция Блоккенкодингбилку

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Кодирует интересующий оператор в `BlockEncoding` .

Создается `BlockEncoding` единая $U = П\кдот В\кдот P ^ \дагжер $, которая кодирует некоторый оператор $H = \ sum_ {j} | \ alpha_j | U_j $, представляющая собой линейное сочетание унитариес. Как правило, $P $ является подготовкой состояния, таким, что $P \кет {0} \_ a = \ sum_j \скрт{\ alpha_j/ \| \век\алфа \| \_ 2} \кет{ж} \_ a $ и $V = \ sum_ {j} \кет{ж}\бра{ж} \_ а\отимес U_j $.

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="statepreparation--t--unit--is-adj--ctl"></a>Статепрепаратион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Единое $P $, которое готовит конечное состояние.


### <a name="selector--ts--unit--is-adj--ctl"></a>селектор: ('T) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Единое $V $, которое кодирует компонент унитариес $H $.



## <a name="output--ts--unit--is-adj--ctl"></a>Выходные данные: ('T) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Единая $U $ взаимодействует с регистрами `a` и `s` кодирует $H $ и соответствует $U ^ \Дагжер = U $.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="s"></a>Возникл



## <a name="remarks"></a>Комментарии

Эта `BlockEncoding` Реализация предоставляет ей свойства `BlockEncodingReflection` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Блоккенкодинг](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. тактов. моделирование. Блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)