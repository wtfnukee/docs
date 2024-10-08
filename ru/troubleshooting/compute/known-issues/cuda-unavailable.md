# Недоступна CUDA на платформе GPU


## Описание проблемы {#issue-description}

CUDA недоступна на платформе GPU.

## Решение {#issue-resolution}

Необходимо выполнить команды:

1. `sudo apt update -y`.
1. `sudo apt upgrade -y`.
1. `pip3 install torch`.

После этого нужно проверить доступность CUDA: `torch.cuda.is_available()`.

Альтернативой может стать вариант использовать [сервис {{ ml-platform-name }}](../../../datasphere/concepts/configurations.md), где используются конфигурации на базе GPU. У каждого проекта сервиса есть несколько Docker-образов с определенным набором ПО. Если этого будет недостаточно, то можно [собрать собственный образ для проекта](../../../datasphere/operations/user-images.md).

{% note info %}

CUDA и cuDNN уже встроены в базовый Docker-образ. 

{% endnote %}

Проверить версию этих компонентов можно двумя командами:

* Проверить версию CUDA: `!nvcc --version`;
* Проверить версию cuDNN: `!cat /usr/include/cudnn_version.h`.

Дополнительно можно узнать:

* Информацию по NVIDIA: `!nvidia-smi`;
* Доступность CUDA через torch: `torch.cuda.is_available()`.
