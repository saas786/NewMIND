---
type: paper
tags: 📥️/📜️ 🖥️
aliases:
  - Файл управления завимсимостями packege.json
---



# Title: **[[PackageJson 2021-10-16]]**


## Metadata:

- `Type:` [[&]]
- `Links:` [[Npm 2021-10-16|Пакетный менеджер npm]], [[Версии 2021-10-16|Версии пакетов npm]]
- `Author:` 
	- `Notable Authors:` 
- `Keywords:` Node js, npm, зависисмости, пакеты, версии, проект.
- `Specific Subject:` Утилиты
- `General Subject:` Node js
- `Reviewed Date:` [[2021-10-16]]


## Notes

### Идея
Основа проекта, данные, скрипты для управления(запуска, дебага), зависимости.

### Скрипты
```javascript
{
	"scripts": {
		"start": "node index.js",
		"dev": "nodemon index.js",
		"<comand>": "<Bash code>"
	},
}
```
Скрипты для управления. Ключом является краткая команда для выполнения, данные это bash скрипт.

```bash
npm start
npm dev
```
Запускается через npm + команда для выполнения.

### Зависимости
#### Для запуска
```javascript
{
	"dependencies": {
		"lodash": "^4.17.21",
		"<package>": "<vesion>"
	}
}
```
Ключом будет пакет, а информацией [[версия 2021-10-16]].

#### Для разработки
```javascript
{
	"devDependencies": {
		...
	}
}
```
Всё как в [[#Для запуска]].