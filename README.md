# kyrochka3

## Задание

Открываем репозиторий на гитхабе:

Clone репозиторий на компьютер 3 раза, симулируя 3 пользователя 


Use mostly command-line (it will be in the test), but also play with gitk to see how it works (not in the test).
For merge I use meld
Добавляем там файл “ryaba.txt” и пишем туда сказку о курочке рябе. Это tag “v1.0”
Скачиваем v1.0 во все 3 локальных репозитория и working directory. 

- user 1:
  - Оздает  бренч “zoya” в котором курицу зовут “Зоя” а дед работает продавцом в Макдаке.
  - В мастере меняет что она живет у двух дедов. 
  - Все изменения пушим на origin
- user 2 
  (не делает git pull или git fetch!)
  - Создает из v1.0  бренч “dusya” в котором вместо курицы Рябы фигурирует корова Дуся, она вместо молока дает что нибудь более интересное. 
  - В мастере курица Ряба в конце истории делает что нибудь неожиданное. Все закоммитить и запушить на origin.
  - Добавляет в мастере что курица ряба - анархистка.  Все закоммитить, но не пушить.
  - Добавляет в мастере что дед яйцо бил каким нибудь предметом.  Все закоммитить, но не пушить.
  - добавляет в мастере что баба яйцо пыталась разбить особенным образом.  Все закоммитить, но не пушить. (если бабы уже  нет, то то что было бабой до изменений)
  - Соединяет свои последние коммиты в 1 с помощью rebase -i, и запушите на сервер
  - Создает локальную ветку “belka” где мышка не бежала, а перебиралась более современным образом. Не пушим “belka”!!
- user 3: 
(не делает git pull или git fetch!)
  - Создает из v1.0 бренч “maga” в котором яйцо разбивает какая нибудь историческая личность. Закоммитить только локально.
  - В master курица Ряба уходит работать на какую нибудь взрослую работу. Комитим. 
  - Синхронизируем с origin/master, не используя команду “pull”, а с помощью fetch и merge.
  - Git push master и maga
- user 2: 
  - Синхронизируется с origin. После этого добавляет ветвь “belka” в origin/master с помощью rebase, без merge. Git push
  - Дает таг origin/master “v1.1”.

***
Часть 2
- user 3:
  Создает ветвь “origin/alternativehistory”,  где он merge zoya и dusya с помощью fetch и merge. Тут есть 3 варианта (так как я не совсем ясно здесь описал а часть людей уже сдали, все версии принимаются как верные): 
либо только их друг с другом (git checkout -b alternativehistory origin/zoya)
либо обе в v1.1
либо обе в то, что у него есть в working directory в данный момент.  
  - Закоммитить и запушить в origin.
  - Merge ветку maga в origin/alternativehistory и в origin/master
  - Добавляет в ветку origin/alternativehistory файл “test1.txt”, куда записывает сказку о колобке. Все это пушит в origin. 
  - Запушить все в origin.
- user 2: 
  - Ему не нравится название файла. Он скачивает ветку origin/alternativehistory к себе, переименовывает файл из test1.txt в kolobok.txt. 
  - Все пушит.

---
---

## English version

## Task

* Open new repository on github
* Clone it to your computer 3 times to different dirs, simulating 3 different users.
* Use mostly command-line (it will be in the test), but also play with gitk to see how it works (not in the test).
* For merge I use meld
* Add file “ryaba.txt” and write there  сказку о курочке рябе. Tag it “v1.0”
* Do “git pull of v1.0 to 3 local repositories and working directory. 
* User 1:
  * Create branch “zoya” whre the chicket named “Зоя” and the ded works at macdonalds.
  * In master the chicken lives with 2 deds. 
  * Push everything to  origin
* User 2 
  (Dont do  git pull or  git fetch at this point)
  * Create from v1.0 brench  “dusya” where instead of Рябы there is cow Дуся, who gives something interesting instead of the milk. 
  * In master Ряба does something unexpected in the end. Commit and push origin.
  * Add in master that ряба is анархистка.  Commit, but dont push.
  * In master, add that ded tried to break the egg with some object.  commit , don’t push.
  * Add that baba (or other ded) tryed to break the egg in an interesting way. Commit, dont push.
  * Squash all 3 commits in to one with  rebase -i, and push to the server
  * Create local branch “belka” where the mouse used transport instead of running. Dont push  “belka” to origin!!
* User 3: 
  (dont git pull или git fetch!)
  Create from v1.0 branch “maga”, where the egg is brocken by someone famous from history. Commit only localy.
  в master the chicken finds a grown up work. commit. 
  Sync with  origin/master, without “pull”: use fetch and then merge masters.
  Git push master and maga
* User 2: 
  * Sync with origin. Then add “belka” to origin/master with rebase, without merge. Git push
  * Tag origin/master “v1.1”.
* User 3:
  * Create branch “origin/alternativehistory”,  where he merges together zoya и dusya with fetch and merge. 3 options are OK: 
  * Merge them with each other (git checkout -b alternativehistory origin/zoya)
  * Merge both to  v1.1
  * Merge both into what you have in your working directory 
  * Commit and push alternativereality to  origin.
  * merge maga into origin/alternativehistory and origin/master
  * Add to branch origin/alternativehistory file “test1.txt”, where we add story about kolobok. 
  * Push to origin.
* User 2: 
  * Pull origin/alternativehistory, rename test1.txt to kolobok.txt. 
  * Push the change.
  
### Done.
