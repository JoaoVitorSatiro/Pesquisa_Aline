> [!NOTE]
> # Pesquisa_Aline
> Nome: Carolina de Oliveira Alves, João Vítor Sátiro Pardin --> 2º Desenvolvimento de Sistemas.
<hr>

 ># Pesquisa sobre permissões e sensores.



## Introdução

Nesta pesquisa abordaremos temas como permissões, actives e sensores dentro do Android Studio, especificando cada um dos temas com diferentes tipos de conceitos, tudo ligado há temas relacionados a funções para que o aparelho móvel funcione do jeito que conhecemos hoje. Tudo por trás de uma tela existem códigos para tudo que realizamos em um dispositivo. Conheceremos um pouco de alguns desses conceitos hoje.


## Sensores do Android Studio

Em todos os dispositivos elétricos existem sensores para fins de auxílio no dia a dia na vida de quem precisa. Entre esses sensores existem tanto no hardware como no software e no Android Studio os sensores são divididos em três tipos:

* `Sensores de Movimento:` capta movimentos de aceleração dos eixos xyz, por exemplo acelerômetro, gravidade, vetor rotacional etc.

* `Sensores de Ambiente:` capta parâmetros ambientais, tudo relacionado a área onde se encontra o aparelho, por exemplo temperatura ambiental, iluminação, umidade, isso inclui também barômetros, fotômetros e termômetros.

* `Sensores de Posição:` medem a posição física/localização do dispositivo, incluem sensores de orientação e magnetômetros.
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

## Permissões do Android Studio

As permissões do app ajudam a apoiar a privacidade do usuário protegendo o seguinte: Dados restritos, como o estado do sistema e os dados de contato dos usuários. Ações restritas, como a conexão a um dispositivo pareado e a gravação de áudio. As permissões necessárias são declaradas com o elemento "<permission>".

* `Permissões normais:` são permissões em que o aplicativo autoria acesso de dados a mais para executar alguma ação dentro de outros aplicativos ou o que está em uso.
* `Permissões de assinatura:` alguns serviços do aplicativo requerem serviços bônus ou privilegiados que o serviço normal não proporciona, assim funciona a assinatura para esses serviços extras.
* `Permissões de execução:` são permissões que concede acesso a outros tipos de ações restritas que podem acabar alterando o sistema implementado do aplicativo, essa permissão necessita do consentimento para acessá-las. 
* `Permissões especiais:` permissões especiais são um conjunto de operações escolhidas pelo usuário mantendo-as ativadas. 
* `Grupo de Permissões:` se baseia em um grupo com permissões que são relacionadas, assim quando o usuário ativar alguma permissão essas permissões relacionadas aparecem na mesma interface.

#### Quais são as principais permissões disponíveis? 

* `Permissão de Localização:` acessa a localização do aparelho.
  
* `Permissão de Câmera:` acessa a câmera para tirar fotos ou gravar vídeos.
* `Permissão de Armazenamento:` acessa o armazenamento do aparelho.
* `Permissão de Microfone:` acessa o microfone para gravar áudio.
* `Permissão de Sensores:` acessa todos os sensores disponíveis no aparelho.
* `Permissão de Contatos:` acessa os contatos do dispositivo.
* `Permissão de Telefone:` acessa o telefone para gerenciar chamadas ou ligações.
* `Permissões de Mensagens:` acessa as mensagens para gerenciar conversas.
* `Permissões de Conexão à Internet:` acessa as conexões de internet para ver registros de wifi.
* `Permissões de Notificações:` acessa notificações para gerenciar notificações do dispositivo.
* `Permissões de instalação:` dão ao app acesso limitado a dados restritos ou permitem que o app execute ações restritas que afetam o sistema ou outros apps.


#### Quais recursos são necessários?

Existem vários recursos apresentados num aplicativo, para complementar conteúdos tudo isso baseado nas configurações do dispositivo e serão apresentados alguns desses recursos logo a seguir:

* `Recursos de animação:` apresentam animações aparentes quando acessadas.
  
* `Recursos de estado de cor:` apresentam mudança de cores com base no estado obtido.
* `Recursos de drawables:` apresentam vários gráficos diferentes no layout.
* `Recursos de layout:` apresentam a interface do aplicativo.
* `Recursos de string:` apresentam diferentes tipos de estilos e formatações para textos.
* `Recursos de ID:` definem um identificador único para componentes do aplicativo.
* `Recursos de menu:` apresenta o menu do aplicativo.


## Actions para uso em intents implícitas.

As actions ou Ações é a definição de como algo deve ser feito ou deve acontecer. As actions no geral em intents implícitas não nomeiam nenhum componente específico, mas declaram o que deve realizar, permitindo que um componente de outro aplicativo qualquer a processe. 

#### Quais são os tipos e finalidades?
```
ACTION_VIEW: é usada quando houver informações de que uma atividade possa ser vizualizada ao usuário, como uma foto para exibição em um aplicativo de galeria.
```
```
ACTION_EDIT: Forneçe acesso para edição de dados fornecidos.
```
```
ACTION_SEND: Usada para o compartilhamento de dados que o usuário possa compartilhar por meio de outro aplicativo.
```
```
ACTION_DIAL: Essa ação é de discar um número que foi informado ao usuario.
```
```
ACTION_CALL: Inicia uma chamada no aplicativo.
```
```
ACTION_SENDTO: Sendo usada para enviar dados a um destino específico.
```
```
ACTION_VIEW_SETTINGS: Essa ação abre a configurações do dispositivo ou aplicativo.
```
```
ACTION_SEARCH: Essa ação executa uma pesquisa.
```
```
ACTION_WEB_SEARCH: Essa ação inicia uma busca na web.
```
```
ACTION_PICK: Sendo usada para permitir que o usuário escolha uma opção de uma lista qualquer.
```
```
ACTION_GET_CONTENT: Permite que o usuário crie os dados enquanto eles são executados, por exemplo, gravar um som.
```
```
ACTION_MAIN: É uma ação princiapl que começa como o ponto de entrada, assim não espera receber dados.
```
```
ACTION_CAMERA: Inicia um aplicativo de câmera para tirar fotos ou gravar vídeos.
```
<hr>

## Conclusão 

Podemos concluir com essa pesquisa os principais tipos de Permissões, Sensores e Actions. Abordamos as permissões essenciais que garantem a segurança e privacidade dos usuários, destacando categorias como localização, câmera, armazenamento e sensores. A compreensão das permissões é crucial para o desenvolvimento responsável de aplicativos, assegurando que as ações restritas sejam executadas com o consentimento adequado. As actions em intents implícitas, oferecendo uma visão abrangente de como as ações orientam o comportamento dos aplicativos. Desde visualizar e editar dados até compartilhar e discar Revelando a complexidade e a interconexão entre permissões, sensores e actions, fundamentais para o desenvolvimento de aplicativos móveis eficientes e respeitosos à privacidade do usuário.
<hr>

## Referências

* https://acervolima.com/como-exibir-a-lista-de-sensores-presentes-em-um-dispositivo-android-programaticamente/

* https://developer.android.com/guide/topics/sensors/sensors_environment?hl=pt-br

* https://developer.android.com/guide/topics/sensors/sensors_position?hl=pt-br

* https://developer.android.com/guide/topics/sensors/sensors_overview?hl=pt-br

* https://developer.android.com/guide/topics/permissions/overview?hl=pt-br

* https://developer.android.com/guide/topics/resources/providing-resources?hl=pt-br

* https://developer.android.com/reference/android/content/Intent#ACTION_SEARCH

* https://developer.android.com/training/camera/camera-intents?hl=pt-br

* https://developer.android.com/training/keyboard-input/style?hl=pt-br

* https://developer.android.com/reference/android/content/Intent#ACTION_DIAL
