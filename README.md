# WhoCame

[![license](https://img.shields.io/github/license/code-418-dpr/WhoCame)](https://opensource.org/licenses/MIT)
[![release](https://img.shields.io/github/v/release/code-418-dpr/WhoCame?include_prereleases)](https://github.com/code-418-dpr/WhoCame/releases)
[![downloads](https://img.shields.io/github/downloads/code-418-dpr/WhoCame/total)](https://github.com/code-418-dpr/WhoCame/releases)
[![code size](https://img.shields.io/github/languages/code-size/code-418-dpr/WhoCame.svg)](https://github.com/code-418-dpr/WhoCame)

Продвинутая система идентификации посетителей

## Особенности реализации

- [x] отсутствие функционала

## Стек

...

## Установка

> [!NOTE]
> Мы отказались от использования `git submodules` и `git subtree` из-за периодически возникающей путаницы при
> отслеживании изменений в монорепозиториях. Данный репозиторий представляет собой единую точку для работы с проектом,
> лишённую этих недостатков.

0. Клонируйте репозиторий и перейдите в его папку.
1. Клонируйте репозитории сервисов, входящих в состав проекта по SSH (рекомендуется):

```shell
git clone git@github.com:code-418-dpr/WhoCame-frontend.git services/frontend
git clone git@github.com:code-418-dpr/WhoCame-backend.git services/backend
git clone git@github.com:code-418-dpr/WhoCame-cv.git services/cv
```

или по HTTPS:

```shell
git clone https://github.com/code-418-dpr/WhoCame-frontend.git services/frontend
git clone https://github.com/code-418-dpr/WhoCame-backend.git services/backend
git clone https://github.com/code-418-dpr/WhoCame-cv.git services/cv
```

После этого вы можете вносить изменения в каждый из сервисов по-отдельности (в соответствии с инструкциями, описанными в
соответствующих README).

## Запуск

0. Установите проект по инструкции выше.
1. Создайте файл `.env` на основе [.env.template](.env.template) и настройте все описанные там параметры.
2. Теперь запускать проект можно командой:

```shell
docker compose up
```
