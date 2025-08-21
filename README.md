<img src="https://github.com/user-attachments/assets/8d2099bb-ad1f-4891-ad39-fe3396adba21" alt="VZOR AI icon" width="15%" />

# VZOR AI

[![license](https://img.shields.io/github/license/code-418-dpr/VZOR)](https://opensource.org/licenses/MIT)
[![release](https://img.shields.io/github/v/release/code-418-dpr/VZOR?include_prereleases)](https://github.com/code-418-dpr/VZOR/releases)
[![downloads](https://img.shields.io/github/downloads/code-418-dpr/VZOR/total)](https://github.com/code-418-dpr/VZOR/releases)
[![code size](https://img.shields.io/github/languages/code-size/code-418-dpr/VZOR.svg)](https://github.com/code-418-dpr/VZOR)

Масштабируемая система интеллектуального анализа изображений

<details>
  <summary><h2>Демо</h2></summary>
  <h3>Лендинг</h3>
  <img width="70%" src="https://github.com/user-attachments/assets/55bd1d39-6fee-4d78-8da8-21291e82a012" />
  <img width="70%" src="https://github.com/user-attachments/assets/8dae60a8-3676-4a3d-b6f2-c5ad7a977341" />
  <img width="70%" src="https://github.com/user-attachments/assets/218ca60f-cdd8-4d33-8671-f32696cdb28d" />
  <img width="70%" src="https://github.com/user-attachments/assets/a3530122-dfc2-45b6-8c2b-61206d741577" />
  <h3>Вход и регистрация, светлая тема</h3>
  <img width="70%" src="https://github.com/user-attachments/assets/77de44db-7856-4a04-8e02-8b32b4995cb4" />
  <img width="70%" src="https://github.com/user-attachments/assets/316c2202-41ee-40bf-aa20-d4d4f39ce7b3" />
  <h3>Основной функционал</h3>
  <h4>Галерея и распознавание</h4>
  <img width="70%" src="https://github.com/user-attachments/assets/ffe8d8e9-d355-42ff-843c-581fc80060f2" />
  <img width="70%" src="https://github.com/user-attachments/assets/3211a2a6-889f-403a-a877-6337bf0cb741" />
  <img width="70%" src="https://github.com/user-attachments/assets/4095e2a9-927d-41df-9dc8-6c66406862fd" />
  <h4>Поиск с искажениями</h4>
  <img width="70%" src="https://github.com/user-attachments/assets/4c1134b3-5d20-4cc5-8a3d-b461359bec75" />
  <img width="70%" src="https://github.com/user-attachments/assets/51665e80-4493-4500-b7d9-08af5c2f0d77" />
  <h4>Редактирование погрешностей работы нейросетей</h4>
  <img width="70%" src="https://github.com/user-attachments/assets/2733e989-10f0-4952-a3ee-fb0bb37e6cdc" />
  <h3>Функционал администратора системы</h3>
  <h4>Блокировка пользователей</h4>
  <img width="70%" src="https://github.com/user-attachments/assets/48d7f2a9-6285-4a41-8ff7-76b27f12a7af" />
</details>

## Особенности реализации

- [x] отсутствие функционала

## Архитектура

Проект состоит из микросервисов, предназначенных для развёртывания в Docker:

- [фронтенд](https://github.com/code-418-dpr/VZOR-frontend)  
- [бэкенд](https://github.com/code-418-dpr/VZOR-backend)
- [сервис CV](https://github.com/code-418-dpr/VZOR-cv)
- PostgreSQL — реляционная база данных
- MongoDB — NoSQL база данных для хранения метаданных об изображениях
- Redis — NoSQL база данных для кэширования
- Minio — файловое S3-хранилище
- Elasticsearch — движок полнотекстового поиска
- Seq — сервис логирования

## Установка

> [!NOTE]
> Мы отказались от использования `git submodules` и `git subtree` из-за периодически возникающей путаницы при
> отслеживании изменений в монорепозиториях. Данный репозиторий представляет собой единую точку для работы с проектом,
> лишённую этих недостатков.

0. Клонируйте репозиторий и перейдите в его папку.
1. Клонируйте репозитории сервисов, входящих в состав проекта по SSH (рекомендуется):

```shell
git clone git@github.com:code-418-dpr/VZOR-frontend.git services/VZOR-frontend
git clone git@github.com:code-418-dpr/VZOR-backend.git services/VZOR-backend
git clone git@github.com:code-418-dpr/VZOR-cv.git services/VZOR-cv
```

или по HTTPS:

```shell
git clone https://github.com/code-418-dpr/VZOR-frontend.git services/VZOR-frontend
git clone https://github.com/code-418-dpr/VZOR-backend.git services/VZOR-backend
git clone https://github.com/code-418-dpr/VZOR-cv.git services/VZOR-cv
```

После этого вы можете вносить изменения в каждый из сервисов по-отдельности (в соответствии с инструкциями, описанными в
соответствующих README).

## Запуск

0. Установите проект по инструкции выше.
1. Создайте файл `.env` на основе [.env.template](.env.template) и настройте все описанные там параметры.
2. Установите Docker.
3. Теперь запускать проект можно командой:

```shell
docker compose up
```
