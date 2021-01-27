---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: Операция Апплйоутеркдкмаддер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: acaa563245bb7c701316d2dfd35b5be03d8e024d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843704"
---
# <a name="applyoutercdkmadder-operation"></a>Операция Апплйоутеркдкмаддер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Обратимая операция "Ripple" на месте, которая используется в операции сложения целых чисел, Рипплекарряддеркдкм ниже.
Учитывая два регистра кубит `xs` и `ys` одинаковую длину, операция применяет последовательность колебаний кнот и ккнот Gates с Кубитс в и, `xs` `ys` как элементы управления и Кубитс в `xs` качестве целевых объектов.

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="xs--littleendian"></a>xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Первый кубит регистр, содержащий элементы управления и целевые объекты.


### <a name="ys--littleendian"></a>ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Второй кубит регистр, участвующий в элементах управления.


### <a name="ancilla--qubit"></a>анЦилла: [кубит](xref:microsoft.quantum.lang-ref.qubit)

АнЦилла кубит, используемый в Рипплекарряддеркдкм, передан в эту операцию.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

- Андрей A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон: "Новая тактовая цепь Ripple — комплексное сложение", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1