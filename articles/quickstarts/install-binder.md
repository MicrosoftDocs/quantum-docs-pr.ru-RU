---
title: Разработка на Q# и Binder
description: Узнайте, как создавать приложения Q# с помощью Binder.
author: bradben
ms.author: v-benbra
ms.date: 9/03/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.binder
no-loc:
- Q#
- $$v
ms.openlocfilehash: f993a1145dd8c01045d4cc7cfd0c98efd574ea78
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90836555"
---
# <a name="develop-with-no-locq-and-binder"></a>Разработка на Q# и Binder

Вы можете использовать Binder для запуска своих записных книжек Jupyter Notebook и предоставления к ним общего доступа по сети.

## <a name="use-binder-with-the-microsoft-qdk-samples"></a>Использование Binder с примерами Microsoft QDK

Чтобы настроить Binder автоматически на использование примеров Microsoft QDK, выполните следующие действия:

1. Откройте браузер и перейдите на страницу https://aka.ms/try-qsharp.
1. На целевой странице **Quantum Development Kit Samples** (Примеры пакета средств разработки Quantum) щелкните **Q# notebook** (Записная книжка Q#), чтобы узнать больше об использовании IQ# для написания собственных записных книжек квантовых приложений.

![Целевая страница QDK](~/media/binder-install.png)

## <a name="use-binder-with-your-own-notebooks-and-repository"></a>Использование Binder с записными книжками и репозиторием

Если у вас уже есть записные книжки в репозитории GitHub, вы можете настроить Binder для работы с ним:

1. Убедитесь, что в корневом каталоге вашего репозитория присутствует файл с именем *Dockerfile*. Файл должен содержать по меньшей мере следующие строки:

    ```bash
    FROM mcr.microsoft.com/quantum/iqsharp-base:0.12.20082513
    
    USER root
    COPY . ${HOME}
    RUN chown -R ${USER} ${HOME}
    
    USER ${USER}
    ```

    > [!NOTE]
    > Вы можете проверить самую актуальную версию IQ# в [заметках о выпуске](xref:microsoft.quantum.relnotes).

    Дополнительные сведения о создании файла Dockerfile см. в [справке по Dockerfile](https://docs.docker.com/engine/reference/builder/).

2. Откройте браузер и перейдите на страницу [mybinder.org](https://mybinder.org).
3. Введите имя репозитория в виде **URL-адреса GitHub** (например, *мое_имя/мой_репозиторий*), и щелкните **launch** (Выполнить).

![Форма MyBinder](~/media/mybinder.png)
    
## <a name="next-steps"></a>Дальнейшие действия

Теперь, когда вы настроили свою среду Binder, вы можете написать и выполнить [свою первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).
