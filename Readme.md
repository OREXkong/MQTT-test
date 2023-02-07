		
				#  Как запустить протокол MQTT #
			
				
В данном случае рассматривается взаимосвязь двух скетчей через [брокер MQTT](https://hub.docker.com/r/emqx/emqx) , а именно

- *reader.py* - скетч, который пишет сообщения и высылает их
- *lestener.py* - скетч, который принимает сообщения
***

Для того чтобы запустить протокол **необходимо**: 

1. Установить python 3.6

*Если уже установлен, то можно проверить версию с помощью ввода в консоль команду *
>**python3 --version**
9. Развернуть локально [брокер MQTT](https://hub.docker.com/r/emqx/emqx)
>**docker run -d --name emqx -p 18083:18083 -p 1883:1883 emqx/emqx:latest**

2. Через установщик пакетов **Pip** для Python нужно установить клиент **Paho Python**, введя в терминал 
>**pip3 install paho-mqtt**

3. Запустить скетч listener.py через терминал
>**python3 listener.py**

4. Запустить скетч reader.py через терминал
>**python3 reader.py**


								
		
