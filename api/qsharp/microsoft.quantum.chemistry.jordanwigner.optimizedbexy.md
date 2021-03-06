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
# <a name="optimizedbexy-operation"></a>Операция Оптимизедбекси

Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Единая $U $, которая применяет строку Паули в $ (X ^ {z + 1} \_ Корр. {z} \_ p) z \_ {p-1}... Z_0 $0.. p $ включено в индекс $z \ин \{ 0, 1 \} $ и $p $. Т. е. $ $ \бегин{алигн} У\кет {z} \ Сисакет {p} \ Сисакет {\ PSI} = \кет{з}\кет{п} (X ^ {z + 1} \_ Корр. {z} \_ p) z \_ {p-1}... Z_0 \кет{\пси} \енд{алигн} $ $

```qsharp
operation OptimizedBEXY (pauliBasis : Qubit, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="paulibasis--qubit"></a>Паулибасис: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Если кубит находится в состоянии $ \кет {0} $, применяется $X $. Когда он находится в состоянии $ \кет {1} $, применяется $Y $.


### <a name="indexregister--littleendian"></a>Индексрегистер: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Состояние $ \кет{п} $ этого регистра определяет кубит, к которому применяется $X $ или $Y $ $.


### <a name="targetregister--qubit"></a>Таржетрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация Кубитс, к которой применяются операторы Паули.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

- Кодирование электронных спектра в тактовых каналах с помощью линейного T сложности Райан Баббуш, Крейг Гиднэй, Dominic W. Берри, (Nathan Виебе, Жаррод Астрид, Александру Палер, Остин Фаулер, Хартмут Невен https://arxiv.org/abs/1805.03662