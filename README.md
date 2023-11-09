> # Pesquisa_Aline
> Nome: Carolina de Oliveira ALves, João Vítor Sátiro Pardin --> 2º Desenvolvimento de Sistemas.
# Pesquisa sobre permissões e sensores.



## Introdução

Nesta pesquisa abordaremos temas como permissões, actives e sensores dentro do Android Studio, especificando cada um dos temas com diferentes tipos de conceitos, tudo ligado há temas relacionados a funções para que o aparelho móvel funcione do jeito que conhecemos hoje. Tudo por trás de uma tela existem códigos para tudo que realizamos em um dispositivo. Conheceremos um pouco de alguns desses conceitos hoje.


## Sensores do Android Studio
Em todos os dispositivos elétricos existem sensores para fins de auxílio no dia a dia na vida de quem precisa. Entre esses sensores existem tanto no hardware como no software e no Android Studio os sensores são divididos em três tipos:
Sensores de Movimento: capta movimentos de aceleração dos eixos xyz, por exemplo acelerômetro, gravidade, vetor rotacional etc.
Sensores de Ambiente: capta parâmetros ambientais, tudo relacionado a área onde se encontra o aparelho, por exemplo temperatura ambiental, iluminação, umidade, isso inclui também barômetros, fotômetros e termômetros.
Sensores de Posição: medem a posição física/localização do dispositivo, incluem sensores de orientação e magnetômetros.
Entre tantos sensores disponíveis nem todos os dispositivos possuem todos os sensores, mas serão apresentados cada um dos sensores e onde cada um se encaixa entre as divisões faladas acima.

#### Os Principais Tipos de Sensores
````
TYPE_ACCELEROMETER: Ele é feito para hardware, serve para medir força de aceleração aplicada entre os eixos xyz em m/s². Também usado para detectar movimentos do dispositivo.
````
````
TYPE_AMBIENT_TEMPERATURA: Ele é feito para hardware, serve para medir a temperatura do ambiente em ºC, monitorando as temperaturas através do ar.
````
````
TYPE_GRAVITY: Ele é feito tanto para hardware tanto para software, serve para medir a gravidade em m/s² é aplicada nos eixos xyz. Também usado para detectar movimentos do dispositivo.
````
````
TYPE_LIGHT: Ele é feito para hardware, serve para detectar ou medir o nível de luz no ambiente, controla o brilho da tela do dispositivo.
````
````
TYPE_MAGNETIC_FIELD: ele é feito para hardware, serve para medir o campo geomagnético do ambiente pelos eixos xyz, criando uma bússola.
````
````
TYPE_ORIENTATION: ele é feito para software, serve para medir o campo de rotação em ºC do dispositivo, determinando a posição do dispositivo.
````
````
TYPE_PRESSURE: feito para hardware, serve para medir a pressão do ar no ambiente, monitorando as mudanças na pressão do ar.
````
````
TYPE_PROXIMITY: feito para hardware, serve para medir a proximidade de um objeto em cm em relação á tela do dispositivo, por exemplo a posição do celular do ouvido de uma pessoa durante uma chamada.
````
````
TYPE_RELATIVE_HUMIDITY: feito para hardware, serve para medir a umidade do ar em porcentagem.
````
````
TYPE_ROTATION_VECTOR: feito para hardware e software, serve para detectar a movimentação do dispositivo informando os três elementos do vetor orientado.
````
````
TYPE_TEMPERATURE: feito para hardware, serve para medir a temperatura do dispositivo em ºC.
````
#### Entre os sensores de movimentação entram:
````
- TYPE_ACCELEROMETER: Ele é feito para hardware, serve para medir força de aceleração aplicada entre os eixos xyz em m/s². Também usado para detectar movimentos do dispositivo.
````
````
- TYPE_ACCELEROMETER_UNCALIBRED: mede a aceleração do eixo xyz, sem compensação de tendência.
````
````
- TYPE_GRAVITY: Ele é feito tanto para hardware tanto para software, serve para medir a gravidade em m/s² é aplicada nos eixos xyz. Também usado para detectar movimentos do dispositivo.
````
````
- TYPE_GYROSCOPE: mede a rotação ao redor dos eixos xyz do dispositivo.
````
````
- TYPE_GYROSCOPE_UNCALIBRATED: mede a rotação ao redor dos eixos xyz do dispositivo (sem compensação de deslocamento).
````
````
- TYPE_LINEAR_ACCELERATION: mede a força de aceleração dos eixos xyz, excluindo a gravidade.
````
````
- TYPE_ROTATION_VECTOR: feito para hardware e software, serve para detectar a movimentação do dispositivo informando os três elementos do vetor orientado.
````
````
- TYPE_STEP_DETECTOR: mede a contagem de passos do usuário desde a última reinicialização.
````
#### Entre os sensores de ambiente entram:
````
- TYPE_AMBIENT_TEMPERATURA: Ele é feito para hardware, serve para medir a temperatura do ambiente em ºC, monitorando as temperaturas através do ar.
````
````
- TYPE_LIGHT: Ele é feito para hardware, serve para detectar ou medir o nível de luz no ambiente, controla o brilho da tela do dispositivo.
````
````
- TYPE_PRESSURE: mede a pressão do ar ambiente.
````
````
- TYPE_RELATIVE_HUMIDITY: feito para hardware, serve para medir a umidade do ar em porcentagem.
````
````
- TYPE_TEMPERATURE: feito para hardware, serve para medir a temperatura do dispositivo em ºC.
````

#### Entre os sensores de posição entram:
````
- TYPE_GAME_ROTATION_VECTOR: mede a rotação do vetor ao longo do eixo x (x * sen (0/2)).
````
````
- TYPE_GEOMAGNETIC_ROTATION_VECTOR: mede a rotação geomagnética detectando os eixos.
````
````
- TYPE_MAGNETIC_FIELD: detecta a intensidade do campo geomagnético dos eixos xyz.
````
````
- TYPE_MAGNETIC_FIELD_UNCALIBRATED: detecta a intensidade do campo geomagnético dos eixos xyz (sem calibragem do ferro duro)
````
````
- TYPE_ORIENTATION: detecta o ângulo da posição do dispositivo nos ângulos xyz.
````
````
- TYPE_PROXIMITY: mede a distância por proximidade de um objeto ao dispositivo em cm.
````


#### *Sintaxe para identificar qualquer sensor no Android Studio: sensorManager = (SensorManager) getSystemService (Context.SENSOR_SERVICE);*


Dentro de tudo isso o framework oferece várias classes e interfaces que ajudam a realizar uma grande variedade de tarefas relacionadas ao sensor. Por exemplo, você pode usar o framework para as seguintes ações:
Determinar quais sensores estão disponíveis em um dispositivo.
Determinar os recursos de um sensor individual, como alcance máximo, fabricante, requisitos de energia e resolução.
Coletar dados brutos do sensor e definir a taxa mínima de velocidade dessa coleta.
Registrar e cancelar o registro dos listeners de eventos que monitoram mudanças do sensor.
Entre essa classe e interfaces o framework inclui:
````
sensorManager: é uma classe que cria instancia, criando métodos para acessar, listar, registrar ou cancelar registros.
````
````
Sensor: é uma classe que cria instâncias específicas de um sensor oferecendo recursos para determinado sensor.
````
````
SensorEvent: é uma classe que cria um objeto para determinado evento, disponibilizando informação desse evento.
````
````
SensorEventListener: usa interface para criar dois métodos de call-back (eventos de entrada) recebendo notificações quando esses eventos mudarem.
````




