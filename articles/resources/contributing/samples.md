---
title: Участвующие примеры для Microsoft КДК
description: Сведения о том, как внести пример кода в Microsoft Quantum Development Kit (КДК).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
no-loc:
- Q#
- $$v
ms.openlocfilehash: ae29614cc9c8bf965ea3cb373dc17470aec21252
ms.sourcegitcommit: 8256ff463eb9319f1933820a36c0838cf1e024e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/17/2020
ms.locfileid: "90759192"
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

То есть образцы в [репозитории Microsoft/такта](https://github.com/microsoft/Quantum) разбиваются по предметной области на разные папки, такие как `algorithms/` , `arithmetic/` или `characterization/` .
В папке для каждой предметной области каждый пример состоит из одной папки, которая собирает все, что пользователю потребуется для изучения и использования этого примера.

## <a name="how-samples-are-structured"></a>Структурирование образцов

Просмотрев файлы, составляющие каждую папку, давайте рассмотрим [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/main/samples/algorithms/chsh-game) пример.

| Файл              | Описание                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | Q# проект, используемый для построения примера с пакет SDK для .NET Core |
| `Game.qs`         | Q# операции и функции для образца                 |
| `Host.cs`         | Управляющая программа C#, используемая для запуска примера                     |
| `host.py`         | Главное приложение Python, используемое для запуска примера                 |
| `README.md`       | Документация о том, что делает пример и как его использовать    |

Не во всех примерах будет один и тот же набор файлов (например, некоторые примеры могут быть только на C#, другие могут не иметь узла Python, или для некоторых примеров может потребоваться работать с файлами данных ауксиллари).

## <a name="anatomy-of-a-helpful-readme-file"></a>Анатомия полезного файла сведений

Тем не менее, особенно важным файлом является `README.md` файл, так как пользователи должны приступить к работе с вашим примером.

Каждый из них `README.md` должен начинаться с некоторых метаданных, которые помогают docs.Microsoft.com/Samples найти вашу публикацию.

> [!div class="nextstepaction"]
> [Посмотрите, как готовится пример ЧШ-Game](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

Эти метаданные предоставляются в виде [заголовка YAML](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) , который указывает, какие языки охватывает ваш образец (обычно это будет, `qsharp` `csharp` и `python` ), и какие продукты ваш образец охватывает (как правило, просто `qdk` ).

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> `page_type: sample`Ключ в заголовке необходим для того, чтобы ваш пример отображался по адресу docs.Microsoft.com/Samples.
> Аналогичным образом `product` , `language` ключи и важны для того, чтобы помочь пользователям найти и запустить пример.

После этого полезно дать краткое введение в том, что делает новый пример:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

Пользователи вашего примера также оценят понимание того, что им нужно для его запуска (например, для пользователей требуется только сам пакет разработки такта, или требуется дополнительное программное обеспечение, например node.js?):

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

Все это на месте, вы можете сообщить пользователям, как запустить пример:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

И, наконец, полезно рассказать пользователям о том, что делает каждый файл в примере, и где их можно найти, чтобы получить дополнительные сведения:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> Обязательно используйте абсолютные URL-адреса, так как ваш пример будет отображаться по другому URL-адресу при подготовке к просмотру в docs.microsoft.com/samples!
