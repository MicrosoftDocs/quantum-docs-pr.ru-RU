---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Операция Аппликонтролледонбитстринг
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 82adc74e23e1d50cb6436176a973fdd1a0eeb3bd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841948"
---
# <a name="applycontrolledonbitstring-operation"></a>Операция Аппликонтролледонбитстринг

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет единую операцию к целевой регистру, контролируя состояние, заданное заданной битовой маской.

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="bits--bool"></a>Разрядность: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Битовая строка для управления данной единой операцией в.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Единая операция, применяемая к целевому регистру.


### <a name="controlregister--qubit"></a>Контролрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр такта, который управляет приложением `oracle` .


### <a name="targetregister--t"></a>Таржетрегистер: 'T

Целевой регистр, передаваемый в `oracle` качестве входных данных.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Remarks

Шаблон, заданный параметром `bits` , может быть короче `controlRegister` , в этом случае дополнительные элементы управления Кубитс игнорируются (то есть не контролируются в $ \кет {0} $ и $ \кет {1} $).
Если `bits` значение больше `controlRegister` , возникает ошибка.

Например, это `bits = [0,1,0,0,1]` означает, что `oracle` применяется только в том случае, если `controlRegister` параметр имеет значение в состоянии $ \кет {0} \кет {1} \кет {0} \кет {0} \кет {1} $.