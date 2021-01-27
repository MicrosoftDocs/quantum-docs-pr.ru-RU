---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: Функция Контролледонбитстринг
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: 176170cc972ca67b812b84f79cf97ba5418be9b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840802"
---
# <a name="controlledonbitstring-function"></a>Функция Контролледонбитстринг

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает единую операцию, которая применяет Oracle к целевой регистрации, если состояние регистра элемента управления соответствует заданной битовой маске.

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a>Описание

Выходные данные этой функции представляют собой операцию, которая может быть представлена единым преобразованием $U $ таким, что \бегин{алигн} U \кет{b_0 b_1 \кдотс b_ {n-1}} \кет{\пси} = \кет{b_0 b_1 \кдотс b_ {n-1}} \отимес \бегин{Касес} V \кет{\пси} & \textrm{if} (b_0 b_1 \cdots b_ {n-1}) = \texttt{BITS} \\ \\ \ket{\psi} & \textrm{otherwise} \end{cases} \end{align}, где $V $ является единым преобразованием, представляющим действие `oracle` операции.

## <a name="input"></a>Входные данные

### <a name="bits--bool"></a>Разрядность: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Битовая строка для управления данной единой операцией в.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Единая операция, применяемая к целевому регистру.



## <a name="output--qubitt--unit--is-adj--ctl"></a>Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Единая операция, которая применяется к `oracle` целевому регистру, если контрольное состояние регистра соответствует битовой маске `bits` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="example"></a>Пример

Следующие фрагменты кода эквивалентны:

```qsharp
(ControlledOnBitString(bits, oracle))(controlRegister, targetRegister);
```

и

```qsharp
within {
    ApplyPauliFromBitString(PauliX, false, bits, controlRegister);
} apply {
    Controlled oracle(controlRegister, targetRegister);
}
```

Следующий код подготавливает состояние $ \фрак {1} {2} (\кет {00} -\кет {01} + \кет {10} + \кет {11} ) $:

```qsharp
using (register = Qubit[2]) {
    ApplyToEach(H, register);
    (ControlledOnBitString([false], Z))(register[0..0], register[1]);
}
```

## <a name="remarks"></a>Remarks

Шаблон, заданный параметром `bits` , может быть короче `controlRegister` , в этом случае дополнительные элементы управления Кубитс игнорируются (то есть не контролируются в $ \кет {0} $ и $ \кет {1} $).
Если `bits` значение больше `controlRegister` , возникает ошибка.

При наличии логического массива `bits` и отдельной операции `oracle` выходные данные этой функции являются операцией, которая выполняет следующие действия:

* Примените `X` операцию к каждому кубит регистру элемента управления, соответствующему `false` элементу объекта `bits` .
* применяется `Controlled oracle` к контрольным и целевым регистрам.
* Примените `X` операцию к каждому кубит контрольного регистра, который соответствует `false` элементу объекта, `bits` чтобы вернуть Контрольный регистр к исходному состоянию.

Выходные данные `Controlled` функтор являются особым случаем, `ControlledOnBitString` где `bits` равно `[true, ..., true]` .