# Практическое задание



### Просмотреть информацию о процессоре и модулях оперативной памяти.

Информация о процессоре ->

```
cat /proc/cpuinfo
```

Увидим большой output касательно нашего процессора, его модель, количество ядер и так далее

Информация о модулях оперативной памяти ->

```sh
lsmod | grep "mem"
async_memcpy           16384  2 raid456,async_raid6_recov
async_tx               16384  5 async_pq,async_memcpy,async_xor,raid456,async_raid6_recov

```


Определить модель жесткого диска.

```sh
user@controlnode1:/$ cat /sys/block/sda/device/model
VBOX HARDDISK
```

### Вывести сведения обо всех платах расширения на шине PCIEx.

```shel
lspci -xxxx
```

Флаг `-xxxx` используется для отображения плат на шине pci_express

### Отключить звуковую карту.

```shel
sudo rmmod snd_intel8x0
```

### Выключить контроллер usb.

```shel
user@controlnode1:/dev/bus/usb/001$ sudo rmmod usbhid
user@controlnode1:/dev/bus/usb/001$ sudo rmmod hid_generic
user@controlnode1:/dev/bus/usb/001$ sudo rmmod hid
user@controlnode1:/dev/bus/usb/001$ lsmod | grep "usb"
```
