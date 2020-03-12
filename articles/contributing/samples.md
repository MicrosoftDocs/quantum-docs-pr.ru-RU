---
title: Участвующие примеры для Microsoft КДК
description: Сведения о том, как внести пример кода в Microsoft Quantum Development Kit (КДК).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
ms.openlocfilehash: 3bd0de04a448c74eea6c3e8e3a15dcbb19f9d705
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2020
ms.locfileid: "79024157"
---
# <a name="contributing-samples-to-the-quantum-development-kit"></a>Участвующие примеры в пакете разработки тактов

Если вы заинтересованы в создании кода в [репозитории примеров](https://github.com/Microsoft/Quantum), благодарим вас за то, что вы пожелаете сделать сообщество разработчиков тактов лучше!

## <a name="the-quantum-development-kit-samples-repository"></a>Репозиторий примеров для пакета разработки тактов

Чтобы помочь вам подготовить публикацию для максимально эффективного использования, полезно ознакомиться с расположением репозитория Samples:

```plaintext
microsoft/Quantum
📁 samples/
  📁 algorithms/
    📁 chsh-game/
      📝 CHSHGame.csproj
      📝 Game.qs
      📝 Host.cs
      📝 host.py
      📝 README.md
     ⋮
  📁 arithmetic/
  📁 characterization/
  📁 chemistry/
   ⋮
```

Это значит, что образцы в [репозитории Microsoft/такта](https://github.com/microsoft/Quantum) разбиваются по предметной области на разные папки, такие как `algorithms/`, `arithmetic/`или `characterization/`.
В папке для каждой предметной области каждый пример состоит из одной папки, которая собирает все, что пользователю потребуется для изучения и использования этого примера.

## <a name="how-samples-are-structured"></a>Структурирование образцов

Просмотрев файлы, составляющие каждую папку, давайте подробно рассмотрим пример [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) .

| Файл              | Description                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | Q # проект, используемый для построения примера с пакет SDK для .NET Core |
| `Game.qs`         | Q # операции и функции для примера                 |
| `Host.cs`         | C#ведущее приложение, используемое для запуска примера                     |
| `host.py`         | Главное приложение Python, используемое для запуска примера                 |
| `README.md`       | Документация о том, что делает пример и как его использовать    |

Не все выборки будут иметь одинаковый набор файлов (например, некоторые примеры могут быть C#только что-либо, другие могут не иметь узла Python, или для некоторых примеров может потребоваться работать с файлами данных ауксиллари).

## <a name="anatomy-of-a-helpful-readme-file"></a>Анатомия полезного файла сведений

Один из особенно важных файлов, однако, является файлом `README.md`, так как именно это необходимо для начала работы с вашим примером.

Каждый `README.md` должен начинаться с некоторых метаданных, которые помогают docs.microsoft.com/samples найти вашу публикацию.

> [!div class="nextstepaction"]
> [Посмотрите, как готовится пример ЧШ-Game](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

Эти метаданные предоставляются в виде [заголовка YAML](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) , который указывает, какие языки охватывает ваш образец (как правило, это `qsharp`, `csharp`и `python`) и какие продукты ваш образец охватывает (как правило, просто `qdk`).

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> Для отображения примера в docs.microsoft.com/samples требуется ключ `page_type: sample` в заголовке.
> Аналогичным образом, ключи `product` и `language` важны для того, чтобы помочь пользователям найти и запустить пример.

После этого полезно дать краткое введение в том, что делает новый пример:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

Пользователи вашего примера также оценят знание того, что им нужно для его запуска (например: сделать так, чтобы пользователям просто был нужен сам пакет разработки такта, или требуется дополнительное программное обеспечение, например node. js?):

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

Все это на месте, вы можете сообщить пользователям, как запустить пример:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

И, наконец, полезно рассказать пользователям о том, что делает каждый файл в примере, и где их можно найти, чтобы получить дополнительные сведения:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> Обязательно используйте абсолютные URL-адреса, так как ваш пример будет отображаться по другому URL-адресу при подготовке к просмотру в docs.microsoft.com/samples!
