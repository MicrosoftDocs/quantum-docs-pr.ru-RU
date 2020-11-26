---
uid: Microsoft.Quantum.Simulation.BlockEncodingReflectionByLCU
title: Функция Блоккенкодингрефлектионбилку
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingReflectionByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncodingReflection`.

  This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: e1247d961a7ebce798106c24c46d924dd6e6d347
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229483"
---
# <a name="blockencodingreflectionbylcu-function"></a>Функция Блоккенкодингрефлектионбилку

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Кодирует интересующий оператор в `BlockEncodingReflection` .

Создается `BlockEncodingReflection` единая $U = П\кдот В\кдот P ^ \дагжер $, которая кодирует некоторый оператор $H = \ sum_ {j} | \ alpha_j | U_j $, представляющая собой линейное сочетание унитариес. Как правило, $P $ является подготовкой состояния, таким, что $P \кет {0} \_ a \ sum_j alpha_j \скрт{\/ \| \век\алфа \| \_ 2} \кет{ж} \_ a $ и $V = \ sum_ {j} \кет{ж}\бра{ж} \_ а\отимес U_j $.

```qsharp
function BlockEncodingReflectionByLCU (statePreparation : (Qubit[] => Unit is Adj + Ctl), selector : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a>Входные данные

### <a name="statepreparation--qubit--unit--is-adj--ctl"></a>Статепрепаратион: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Единое $P $, которое готовит конечное состояние.


### <a name="selector--qubitqubit--unit--is-adj--ctl"></a>Selector: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Единое $V $, которое кодирует компонент унитариес $H $.



## <a name="output--blockencodingreflection"></a>Выходные данные: [блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

Единая $U $, взаимодействующая с регистрами `a` и `s` которая кодирует $H $, и соответствует $U "^ {-1} = U $.

## <a name="remarks"></a>Комментарии

Эта `BlockEncoding` Реализация предоставляет ей свойства `BlockEncodingReflection` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Блоккенкодинг](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. тактов. моделирование. Блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)