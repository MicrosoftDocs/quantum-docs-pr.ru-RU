---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Определяемый пользователем тип Секуентиалмодел
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: ab9c121884e489b5d056285008c91c1ad70bb053
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854893"
---
# <a name="sequentialmodel-user-defined-type"></a>Определяемый пользователем тип Секуентиалмодел

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Описывает модель классификатора такта, состоящую из последовательности параметризованных и контролируемых поворотов, присваивания углов поворота и смещения между двумя классами, распознаваемыми моделью.

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a>Именованные элементы

### <a name="structure--controlledrotation"></a>Структура: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Последовательность управляемых поворотов, используемых для классификации входных данных.
### <a name="parameters--double"></a>Параметры: [Double](xref:microsoft.quantum.lang-ref.double)[]

Присваивание углов поворота к заданной структуре классификации.
### <a name="bias--double"></a>Уровень смещения: [Double](xref:microsoft.quantum.lang-ref.double)

Сдвиг между двумя классами, распознаваемыми этим классификатором.

## <a name="references"></a>Ссылки

- [Арксив: 1804.00633](https://arxiv.org/abs/1804.00633)