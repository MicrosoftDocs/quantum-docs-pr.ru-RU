---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Операция Препареуниформсуперпоситион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: dc9d4ce1638b397748cafaa757241ce78633c67c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854322"
---
# <a name="prepareuniformsuperposition-operation"></a>Операция Препареуниформсуперпоситион

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Создает равномерное перестановку по состояниям, закодированным с 0 по `nIndices - 1` .

То есть, это единое $U $ создает равномерное перестановку для всех состояний $0 $ в $M-$1, учитывая входное состояние $ \ket{0\cdots 0} $. Иными словами, $ $ \бегин{алигн} У\кет {0} = \фрак {1} {\скрт{м}}\ sum_ {j = 0} ^ {M-1} \кет{ж}.
\енд{алигн} $ $.

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="nindices--int"></a>Ниндицес: [int](xref:microsoft.quantum.lang-ref.int)

Требуемое число Штатов $M $ в равномерном положении.


### <a name="indexregister--littleendian"></a>Индексрегистер: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр кубит, в котором хранятся числовые состояния в `LittleEndian` формате.
Этот регистр должен иметь возможность хранить число $M-$1, а предполагается, что оно инициализировано в состоянии $ \ket{0\cdots 0} $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Пример

В следующем примере выполняется подготовка состояния $ \фрак {1} {\скрт {6} } \ sum_ {j = 0} ^ {5} \кет{ж} $ on $3 $ Кубитс.

```qsharp
let nIndices = 6;
using(indexRegister = Qubit[3]) {
    PrepareUniformSuperposition(nIndices, LittleEndian(indexRegister));
    // ...
}
```

## <a name="remarks"></a>Remarks

Операция является аджоинтабле, но требует, чтобы `indexRegister` она наглядела в равномерном положении на первом `nIndices` уровне в этом случае.