<h1 align="center"> Ativação de LED RGB por meio de alarmes de hardware em Raspberry Pico W</h1>

## Sobre o projeto

O código implementado neste projeto ativa o LED RGB sequência específica a partir do acionamento de um pushbutton. O software foi desenvolvido para a plataforma 
Raspberry Pico W por meio da Raspberry SDK.
> [!NOTE] 
> Sequência de ativação dos LEDS
> - Etapa 1: ativação dos três LEDs
> - Delay de 3s
> - Etapa 2: ativação dos LEDs verde e azul (led vermelho é desativado)
> - Delay de 3s
> - Etapa 2: ativação dos LEDs azul (led vermelho e verde são desativados)
> - Delay de 3s
> - Etapa 3: Desativação dos três LEDs

Para uma melhor performance do código, realizou-se a temporização por meio de timers de hardware. Foi desenvolvido também uma atenuação em software para o fenômeno
de bouncing do pushbutton.

## Componentes utilizados
- Raspberry Pico W;
- 3 resistores de 330 ohms;
- 3 leds (vermelho, verde e azul) ou 1 led RGB;
- 1 pushbutton
- Plataforma BitDogLag (para teste em hardware físico)


## Instruções de uso


### Clone o repositório
No seu teminal, digite o seguinte comando:

<code> git clone https://github.com/camilaqPereira/embarcatech_timer2.git </code>

### Importe o projeto no VSCode
No VSCode, importe o projeto utilizando a extensão oficial Rasberry Pi

### Compile o projeto
Compile o projeto utilizando o botão **COMPILE** no fim da página (ou **RUN** caso sua placa já esteja conectada ao computador em modo boot)

### Rode o código
Caso tenha gravado o código na placa seguindo o passo anterior, basta pressionar o pushbutton que os LED serão ativados.
Caso deseje simular o funcionamento no Wokwi, basta abrir o arquivo _diagram.json_ e pressionar _play_

## Testes

### [Simulação no Wokwi for VSCode](https://drive.google.com/file/d/1m8Zx33OUe4jr2O6RRjAhpuDSFkFYEdBp/view?usp=sharing)


### [Simulação na placa BitDogLab](https://drive.google.com/file/d/1hMW1PR9f1rV_vaptrO4l3qrQ7kGxn9Da/view?usp=sharing)


>[!NOTE]
>- Vermelho + verde + azul = branco
>- Verde + azul = ciano
