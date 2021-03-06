---
uid: Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance
title: Операция Ассерткубитисинстатевисинтолеранце
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitIsInStateWithinTolerance
qsharp.summary: >-
  Asserts that a qubit in the expected state.

  `expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$. The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part. The last argument defines the tolerance with which assertion is made.
ms.openlocfilehash: b40c5c4f731190c8c0d00d33718680e5448bf767
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829782"
---
# <a name="assertqubitisinstatewithintolerance-operation"></a>Операция Ассерткубитисинстатевисинтолеранце

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Утверждает, что кубит находится в ожидаемом состоянии.

`expected` представляет сложный вектор, $ \кет{\пси} = \бегин{бматрикс}а & б\енд {бматрикс} ^ {\Масрм{т}} $.
Первый элемент кортежей, представляющий каждый из $a $, $b $ является реальной частью комплексного числа, а второй — мнимой частью.
Последний аргумент определяет допуск, с которым выполняется утверждение.

```qsharp
operation AssertQubitIsInStateWithinTolerance (expected : (Microsoft.Quantum.Math.Complex, Microsoft.Quantum.Math.Complex), register : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a>Входные данные

### <a name="expected--complexcomplex"></a>ожидалось: ([сложное](xref:Microsoft.Quantum.Math.Complex),[сложное](xref:Microsoft.Quantum.Math.Complex))

Ожидаемые сложные амплитуды для $ \кет {0} $ и $ \кет {1} $ соответственно.


### <a name="register--qubit"></a>Регистрация: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, состояние которого должно быть утверждено. Обратите внимание, что предполагается, что кубит отделяемых из других выделенных Кубитс, а не запутанными.


### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Аддитивная погрешность, с которой действительные амплитуды могут отклоняться от ожидаемого.
Дополнительные сведения см. в примечаниях ниже.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Пример

```qsharp
using (qubits = Qubit[2]) {
    // Both qubits are initialized as |0〉: a=(1 + 0*i), b=(0 + 0*i)
    AssertQubitIsInStateWithinTolerance((Complex(1., 0.), Complex(0., 0.)), qubits[0], 1e-5);
    AssertQubitIsInStateWithinTolerance((Complex(1., 0.), Complex(0., 0.)), qubits[1], 1e-5);
    Y(qubits[1]);
    // Y |0〉 = i |1〉: a=(0 + 0*i), b=(0 + 1*i)
    AssertQubitIsInStateWithinTolerance((Complex(0., 0.), Complex(0., 1.)), qubits[1], 1e-5);
}
```

## <a name="remarks"></a>Remarks

Следующий код Масематика можно использовать для проверки выражений для MI, MX, My, MZ:

```mathematica
{Id, X, Y, Z} = Table[PauliMatrix[k], {k, 0, 3}];
st = {{ reA + I imA }, { reB + I imB} };
M = st . ConjugateTranspose[st];
mx = Tr[M.X] // ComplexExpand;
my = Tr[M.Y] // ComplexExpand;
mz = Tr[M.Z] // ComplexExpand;
mi = Tr[M.Id] // ComplexExpand;
2 m == Id mi + X mx + Z mz + Y my // ComplexExpand // Simplify
```

Допуск — это $L \_ {\инфти} $ Distance между трехмерным реальным вектором (x ₂, x ₃, x ₄), определяемый $ \лангле\пси | \пси\рангле = x \_ 1 I + x \_ 2 x + x \_ 3 Y + x \_ 4 Z $ и вещественный вектор (y ₂, y ₃, Y ₄), определенный p = y ₁ I + y ₂ x + y ₃ Y + y ₄ Z, где p — это матрица плотности, соответствующая состоянию регистра.
Это справедливо только в случае предположения, что TR (p) и TR (| ψ ⟩ ⟨ ψ |) равны 1 (например, x ₁ = 1/2, y ₁ = 1/2).
Если это не так, функция утверждает, что l ∞ расстояние между (x ₂-x ₁, x ₃-x ₁, x ₄-x ₁, x ₄ + x ₁) и (y ₂-y ₁, y ₃-y ₁, y ₄-y ₁, y ₄ + y ₁) меньше, чем параметр допуска.