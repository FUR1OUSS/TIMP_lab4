**Лабораторная работа №4**

Создаём *fork* репозитория LAB3

Создаём локальный репозиторий и делаем **pull**

Создам workflow:
```
$ mkdir .github
$ cd .github
$ mkdir workflows 
$ cd workflows
$ touch git-action.yaml
```
Вносим изменения:```$ nano git-action.yaml```

<img width="682" alt="Снимок экрана 2023-05-31 в 21 29 21" src="https://github.com/FUR1OUSS/TIMP_lab4/assets/82472327/d54165a5-ec6b-4ba6-816f-eb78bed5ceb2">

Отправляем изменения в удаленный репозиторий:
```
$ git add .github
$ git commit -m "git-action.yaml created"
$ git push origin master
```

<img width="811" alt="Снимок экрана 2023-05-31 в 23 22 37" src="https://github.com/FUR1OUSS/TIMP_lab4/assets/82472327/c1b67309-3d81-49e2-868d-80bf2b974283">
