# Базовые изображения Docker

Этот репозиторий создает и публикует мои базовые образы Docker, которые я использую во всех других своих проектах.

** Я не рекомендую вам использовать эти изображения в ваших собственных проектах, поскольку они адаптированы к моим потребностям!**

## Распределения

Это образы дистрибутива Linux, которые я использую в качестве основы для всех остальных своих образов.

Эти образы создаются из архивных файлов корневой файловой системы и всегда будут использовать последнюю стабильную версию для каждого основного выпуска. Существуют варианты для 64-разрядной x86 и 64-разрядной ARM.

В эти изображения были внесены следующие изменения:
* Переключен на зеркальное отображение репозитория пакетов в Соединенном Королевстве.
* Переключен на британскую английскую локаль и набор символов UTF-8.
* Переключен на часовой пояс UTC.
* Установленные общедоступные сертификаты CA и мой [личный корневой сертификат CA] (контекст/viral32111.элт).
* Установил мой [container healthcheck] [проверка работоспособности контейнера](https://github.com/viral32111/healthcheck ) полезность.
* Создал стандартного непривилегированного пользователя и группу (UID & GID: `1000`).
* Добавлены двоичные файлы локального пользователя в системный путь.
* Отключена запись истории оболочки в файл.

| Название | Версия | Название изображения и тег | Примечание |
| ----- | ------- | ---------------- | ---- |
| [Ubuntu 18.04](https://www.releases.ubuntu.com/bionic /) | 18.04.6 | [`ghcr.io/viral32111/ubuntu:18.04`](https://github.com/viral32111/docker-base-images/pkgs/container/ubuntu ) | LTS. |
| [Ubuntu 20.04](https://www.releases.ubuntu.com/focal /) | 20.04.6 | [`ghcr.io/viral32111/ubuntu:20.04`](https://github.com/viral32111/docker-base-images/pkgs/container/ubuntu ) | LTS. |
| [Ubuntu 22.04](https://www.releases.ubuntu.com/jammy /) | 22.04.3 | [`ghcr.io/viral32111/ubuntu:22.04`](https://github.com/viral32111/docker-base-images/pkgs/container/ubuntu ) | LTS. |
| ~~[Ubuntu 22.10](https://www.releases.ubuntu.com/kinetic/)~~ | ~~22.10~~ | ~~[`ghcr.io/viral32111/ubuntu:22.10`](https://github.com/viral32111/docker-base-images/pkgs/container/ubuntu)~ ~ | ЭОЛ. |
| [Ubuntu 23.04](https://www.releases.ubuntu.com/lunar /) | 23.04 | [`ghcr.io/viral32111/ubuntu:23.04`](https://github.com/viral32111/docker-base-images/pkgs/container/ubuntu ) | |

| Название | Версия | Название изображения и тег | Примечание |
| ----- | ------- | ---------------- | ---- |
| ~~[Alpine Linux 3.15](https://alpinelinux.org/)~~ | ~~3.15.6~~ | ~~[`ghcr.io/viral32111/alpine:3.15`](https://github.com/viral32111/docker-base-images/pkgs/container/alpine)~ ~ | ЭОЛ. |
| [Alpine Linux 3.16](https://alpinelinux.org /) | 3.16.7 | [`ghcr.io/viral32111/alpine:3.16`](https://github.com/viral32111/docker-base-images/pkgs/container/alpine ) | |
| [Alpine Linux 3.17](https://alpinelinux.org /) | 3.17.5 | [`ghcr.io/viral32111/alpine:3.17`](https://github.com/viral32111/docker-base-images/pkgs/container/alpine ) | |
| [Alpine Linux 3.18](https://alpinelinux.org /) | 3.18.3 | [`ghcr.io/viral32111/alpine:3.18`](https://github.com/viral32111/docker-base-images/pkgs/container/alpine ) | |

## Java

В этих изображениях используется Java из [Adoptium Temurin](https://adoptium.net/temurin/releases /), и всегда будет использовать последнюю стабильную версию для каждого основного выпуска.

Эти образы основаны как на Ubuntu 23.04, так и на Alpine Linux 3.18 для 64-разрядной версии x86.

| Название | Версия | Название изображения и тег | Примечание |
| ----- | ------- | ---------------- | ---- |
| [Java 8](https://adoptium.net) | 8u382-b05 | [`ghcr.io/viral32111/java:8`](https://github.com/viral32111/docker-base-images/pkgs/container/java) | |
| [Java 11](https://adoptium.net) | 11.0.20.1+1 | [`ghcr.io/viral32111/java:11`](https://github.com/viral32111/docker-base-images/pkgs/container/java) | |
| [Java 16](https://adoptium.net) | 16.0.2+7 | [`ghcr.io/viral32111/java:16`](https://github.com/viral32111/docker-base-images/pkgs/container/java) | Использует JDK вместо JRE. |
| [Java 17](https://adoptium.net ) | 17.0.8.1+1 | [`ghcr.io/viral32111/java:17 `](https://github.com/viral32111/docker-base-images/pkgs/container/java ) | LTS. |
| [Java 18](https://adoptium.net ) | 18.0.2.1+1 | [`ghcr.io/viral32111/java:18 `](https://github.com/viral32111/docker-base-images/pkgs/container/java ) | |
| [Java 19](https://adoptium.net ) | 19.0.2+7 | [`ghcr.io/viral32111/java:19 `](https://github.com/viral32111/docker-base-images/pkgs/container/java ) | |
| [Java 20](https://adoptium.net ) | 20.0.2+9 | [`ghcr.io/viral32111/java:20 `](https://github.com/viral32111/docker-base-images/pkgs/container/java ) | |

## .NET

Эти образы основаны как на Ubuntu 23.04, так и на Alpine Linux 3.18 для 64-разрядной версии x86.

| Название | Версия | Название изображения и тег | Примечание |
| ----- | ------- | ---------------- | ---- |
| [.NET Runtime 6.0](https://dotnet.microsoft.com/en-us/download/dotnet/6.0 ) | 6.0.22 | [`ghcr.io/viral32111/dotnet:6`](https://github.com/viral32111/docker-base-images/pkgs/container/dotnet ) | LTS. |
| [.NET Runtime 7.0](https://dotnet.microsoft.com/en-us/download/dotnet/7.0 ) | 7.0.11 | [`ghcr.io/viral32111/dotnet:7`](https://github.com/viral32111/docker-base-images/pkgs/container/dotnet ) | |

| Название | Версия | Название изображения и тег | Примечание |
| ----- | ------- | ---------------- | ---- |
| [ASP.NET Core Runtime 6.0](https://dotnet.microsoft.com/en-us/download/dotnet/6.0 ) | 6.0.22 | [`ghcr.io/viral32111/aspnetcore:6`](https://github.com/viral32111/docker-base-images/pkgs/container/aspnetcore ) | LTS. |
| [ASP.NET Core Runtime 7.0](https://dotnet.microsoft.com/en-us/download/dotnet/7.0 ) | 7.0.11 | [`ghcr.io/viral32111/aspnetcore:7`](https://github.com/viral32111/docker-base-images/pkgs/container/aspnetcore ) | |

## Узел.JS

Эти образы основаны как на Ubuntu 23.04, так и на Alpine Linux 3.18 для 64-разрядной версии x86.

| Название | Версия | Название изображения и тег | Примечание |
| ----- | ------- | ---------------- | ---- |
| [Узел.js v18](https://nodejs.org ) | 18.17.1 | [`ghcr.io/viral32111/nodejs:18`](https://github.com/viral32111/docker-base-images/pkgs/container/nodejs ) | LTS. |
| ~~[Узел.js v19](https://nodejs.org)~~ | ~~19.9.0~~ | ~~[`ghcr.io/viral32111/nodejs:19`](https://github.com/viral32111/docker-base-images/pkgs/container/nodejs)~ ~ | ЭОЛ. |
| [Узел.js v20](https://nodejs.org ) | 20.6.1 | [`ghcr.io/viral32111/nodejs:20`](https://github.com/viral32111/docker-base-images/pkgs/container/nodejs ) | |