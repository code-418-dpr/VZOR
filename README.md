<img src="https://github.com/user-attachments/assets/8d2099bb-ad1f-4891-ad39-fe3396adba21" alt="VZOR AI icon" width="15%" />

# VZOR AI

[![license](https://img.shields.io/github/license/code-418-dpr/VZOR)](https://opensource.org/licenses/MIT)
[![release](https://img.shields.io/github/v/release/code-418-dpr/VZOR?include_prereleases)](https://github.com/code-418-dpr/VZOR/releases)
[![downloads](https://img.shields.io/github/downloads/code-418-dpr/VZOR/total)](https://github.com/code-418-dpr/VZOR/releases)
[![code size](https://img.shields.io/github/languages/code-size/code-418-dpr/VZOR.svg)](https://github.com/code-418-dpr/VZOR)

Масштабируемая система интеллектуального анализа изображений

## Особенности реализации

- [x] микросервисная архитектура
- [x] единая среда развёртывания
- [x] интегрирован CI/CD
- [x] веб-приложение с поддержкой технологии PWA
- [x] модульно-монолитный бэкенд на основе архитектуры clean architecture
- [x] несколько нейросетей для работы с изображениями и текстом

## Архитектура

Проект состоит из микросервисов, предназначенных для развёртывания в Docker:

- [фронтенд](https://github.com/code-418-dpr/VZOR-frontend)  
- [бэкенд](https://github.com/code-418-dpr/VZOR-backend)
- [сервис CV](https://github.com/code-418-dpr/VZOR-cv)

## Установка

> [!NOTE]
> Мы отказались от использования `git submodules` и `git subtree` из-за периодически возникающей путаницы при
> отслеживании изменений в монорепозиториях. Данный репозиторий представляет собой единую точку для работы с проектом,
> лишённую этих недостатков.

0. Клонируйте репозиторий и перейдите в его папку.
1. Клонируйте репозитории сервисов, входящих в состав проекта по SSH (рекомендуется):

```shell
git clone git@github.com:code-418-dpr/VZOR-frontend.git services/frontend
git clone git@github.com:code-418-dpr/VZOR-backend.git services/backend
git clone git@github.com:code-418-dpr/VZOR-cv.git services/cv
```

или по HTTPS:

```shell
git clone https://github.com/code-418-dpr/VZOR-frontend.git services/frontend
git clone https://github.com/code-418-dpr/VZOR-backend.git services/backend
git clone https://github.com/code-418-dpr/VZOR-cv.git services/cv
```

После этого вы можете вносить изменения в каждый из сервисов по-отдельности (в соответствии с инструкциями, описанными в
соответствующих README).
2. Запустить проект можно командой
```shell
docker-compose up -d --build
```

## Запуск

0. Установите проект по инструкции выше.
1. Создайте файл `.env` на основе [.env.template](.env.template) и настройте все описанные там параметры.
2. Установите Docker.
3. Теперь запускать проект можно командой:

```shell
docker compose up
```
