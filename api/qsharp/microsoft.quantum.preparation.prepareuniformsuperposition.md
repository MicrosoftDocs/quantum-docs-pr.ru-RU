---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Операция Препареуниформсуперпоситион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: 9b9f182ed7c1ea24ae74b8a2321a309042a17c97
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230095"
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



## <a name="remarks"></a>Комментарии

Операция является аджоинтабле, но требует, чтобы `indexRegister` она наглядела в равномерном положении на первом `nIndices` уровне в этом случае.