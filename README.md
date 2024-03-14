# EnigmaIRC
**Содержание:**
1. [О проекте](#p1)
    - [Что это такое?](#p1_1)
    - [Как это устроено](#p1_2)
2. [Как установить на сервер](#p2)
3. Как настроить клиент

<h2 id="p1">О проекте</h2>
<h3 id="p1_1">Что это такое?</h3>
EnigmaIRC - примитивный мессенджер для обмена сообщениями между небольшим количеством пользователей, использующее симметричное шифрование и рассчитаный на защищённый обмен информацией.

<h3 id="p1_2">Как это устроено</h3>
Главным аспектом EnigmaIRC является <u>ручной обмен ключами шифрования</u>, а также исключительно локальный процесс шифрованя, при котором в сеть уходят только прошедшии процесс шифрования данные.

<h2 id="p2">Как установить на сервер</h2>
В качестве сервера может выступать как арендованый выделенный сервер, так и личных хост. Рекомендованой ОС для сервера является Debian версии 9 и выше, но подойдёт и любая другая система, которая поддерживает Python 3.9+.

Пример установки серверной части EnigmaIRC показана на примере Debian 11.

Обновите список доступных пакетов:

`sudo apt update && sudo apt upgrade --yes`

Установите Python, pip и git:

```
sudo apt install python3
sudo apt install python3-pip
sudo apt install git
```

Скопируйте к себе репозиторий EnigmaIRC:

```
git clone https://github.com/Dertfin3051/EnigmaIRC.git
```

Перейдите в папку с сервером EnigmaIRC и установите все нужные дополнения:

```
cd EnigmaIRC/server
pip install -r requirements.txt
```

Теперь сервер можно запустить!

```
python3 server.py
```