1. Скачиваем с оф.сайта последнюю версию
2. Устанавливаем:
```bash
sudo dpkg -i virtualbox-7.0_0.16-162802~Debian~bookworm_amd64.deb
sudo apt install -f
```
3. Устанавливаем загловки
```bash
sudo apt install linux-headers-`uname -r`
sudo dpkg-reconfigure virtualbox-dkms
sudo modprobe vboxdrv
```
Добавление пользователя в группу:
```bash
sudo usermod -G vboxusers -a zampolit
```

Просмотр групп пользователя
```bash
groups zampolit
```
Установка дополнений гостевой ОС
Перед запуском гостевой ОС переходим в настройки VBox
Настроить => Носители => SATA => Добавить
Добавляем привод из /usr/share/virtualbox/VBoxGuestAdditions.iso
```bash

