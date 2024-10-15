# Índice

- [Aula 1 - Programação em Arduino e Eletrônica Básica](#1)
  - [Autoestudos](#1-autoestudo)
  - [Instrução](#1-instrucao)
  - [Ponderada](#1-ponderada)

---

## <a name="1"></a> Aula 1 - Programação em Arduino e Eletrônica Básica
&nbsp;&nbsp;&nbsp;&nbsp;Resumo: 
<br>

### <a name="1-autoestudo"></a> Aula 1 - Programação em Arduino e Eletrônica Básica - Autoestudos


#### **Instalação de ambiente 1: Como instalar e se familiarizando com as funcionalidades**
- Instalando Arduino IDE
- `Sketch`
    - Compilar/Verificar - Botão no canto superior esquerdo
    - Upload - Botão do lado do de verificação
    - 
- `Tools`
    - Selecionar a placa de arduino que será utilizada (board)
    - Selecionar a porta (identificável assim que o Arduino é conectado. Acessar também o [Gerenciador de Dispositivos](#gerenciador) para verificar as portas)


##### <a name="gerenciador"></a> Acessando o gerenciador de dispositivos
- Windows + R
- Digitar `devmgmt.msc`
- Enter

#### **Instalação de ambiente 2: Pisca LED**
- 💡 O projeto consiste em fazer um LED piscar em intervalos.
- 🔌 Precisamos de uma placa Arduino Uno, cabo USB, LED, resistor, protoboard e fios Jumper.
- ⚙️ Conectamos o Arduino à protoboard e ao LED
    1. Jumper preto no pino GND e conectar na Protoboard (canto inferior esquerdo perto do "+")
    2. Jumper vermelho no pino 10 e na Protoboard contar 6 "furinhos" e conectar
    3. A perna menor do LED alinhada com o preto (GND)
    4. Colocar o resistor alinhado ao jumper vermelho e a outra ponta alinhada com a perna maior do LED
<div align="center">
<sub>Esquema final:</sub>
<br>
<img src="./../img/piscaled.png" alt="">
<br>
</div>
-   💻 Utilizaremos a IDE do Arduino para programar o LED.
    -   📝 O código inclui métodos setup e loop para controlar o LED.

```
// executado ao programa iniciar. Configurações utilizadas no projeto
void setup () {
    pinMode(10, OUTPUT); // Se referencia ao pino 10, output será um pino de saída
}

// Ficará rodando continuamente
void loop() {
    digitalWrite(10, HIGH); // Vai mandar energia para a porta 10
    delay(1000); // Espera 1000 ms
    digitalWrite(10, LOW); // Vai tirar a energia da porta 10
    delay(1000);
}
```
- 🚀 Pronto! O LED começa a piscar em intervalos de um segundo.

##### Considerações
- 🔗 O uso de protoboard facilita a montagem de circuitos, permitindo testar conexões sem soldagem, o que é ideal para iniciantes.
- 📜 A programação em C na IDE do Arduino é intuitiva, com comentários que ajudam a entender o funcionamento do código.
- 🔄 O método loop é fundamental, pois controla a execução contínua das funções, permitindo que o LED pisque indefinidamente.
- ✅ A verificação e compilação do código são etapas cruciais para garantir que o programa funcione corretamente antes de carregar no Arduino.
- 📶 A conexão com o computador e o upload do código são simples, tornando o processo acessível para todos.


#### **Instalação de ambiente 3: Pode resistor no negativo do LED?**

💡 Resistor no terminal negativo é válido.
🔌 A corrente elétrica é o que deve ser controlado.
⚡ Tensão não é o mesmo que corrente.
🔄 Troca de posição do resistor não altera o funcionamento.
🔥 LED pode queimar sem resistor.

##### Considerações
⚙️ **Função do Resistor:** O resistor tem a função específica de limitar a corrente no circuito, protegendo o LED de danos. Sem ele, a corrente excessiva pode levar à queima do LED.
🔍 **Corrente vs. Tensão:** É essencial distinguir entre corrente (medida em amperes) e tensão (medida em volts). A tensão é a diferença de elétrons entre os terminais, enquanto a corrente é o fluxo desses elétrons.
🔄 **Posição do Resistor:** A posição do resistor (positivo ou negativo) não impacta o funcionamento do circuito, pois ele reduz a corrente independentemente de onde esteja.
💧 **Analogias com Água:** Comparar corrente elétrica com fluxo de água ajuda a entender que, ao restringir a passagem em um ponto do circuito, a corrente é reduzida por todo o circuito.
🔥 **Riscos de Não Usar Resistor:** Testes demonstram que conectar um LED sem resistor pode resultar em danos imediatos ao componente, evidenciando a importância do resistor na proteção do circuito.
🛠️ **Importância da Prática:** A abordagem prática utilizada no vídeo ajuda a solidificar a compreensão dos conceitos teóricos, tornando o aprendizado mais eficaz.
📊 **Educação em Eletrônica:** A clareza em conceitos como corrente e tensão é fundamental para quem deseja trabalhar com eletrônica, como em projetos envolvendo Arduino.
<div align="center">
<sub>Como identificar a resistência dos resistores:</sub>
<br>
<img src="./../img/resistores.png" alt="">
<br>
</div>

#### **Instalação de ambiente 4: Componentes eletrônicos**

- ⚙️ **Função dos Componentes:** Componentes como resistores e capacitores são essenciais para controlar a corrente elétrica, transformando-a em luz, som ou movimento, crucial em circuitos eletrônicos.
- 📊 **Diagramas Esquemáticos:** Utilizar diagramas facilita a compreensão e montagem de circuitos complexos, permitindo que até iniciantes planejem suas criações eletrônicas de forma organizada.

<div align="center">
<img src="./../img/diagramaesquematico.png" alt="">
<br>
</div>

<br>

- 🔍 **Identificação de Componentes:** Conhecer os símbolos e funções dos componentes é vital para a montagem de circuitos, promovendo um entendimento mais profundo da eletrônica.
<div align="center">
<sub>Fontes:</sub>
<br>
<img src="./../img/fonte.png" alt="">
<br>
</div>

- 1º: Pilha ou bateria
    - Polo negativo: traço pequeno
    - Polo positivo: traço grande
- 2º: Fonte transformadora
    - COrrente alternada -> corrente contínua
- 3º: Fonte de corrente alternada
    - O `~` representa a corrente alternada

<br>

<div align="center">
<sub>Resistores:</sub>
<br>
<img src="./../img/resistor.png" alt="">
<br>
</div>

- Controla a corrente elétrica
- Aplicativo `Resistor Code Calculator` ajuda a ver qual é a resistência
- Faixa prateada/dourada na extremidade da **direita**
- Resistores com variação de resistências...

<div align="center">
<sub>Potenciômetros!</sub>
<br>
<img src="./../img/potenciometro.png" alt="">
<br>
</div>
- Pista de grafite que alterna a resistência conforme a distância da "flechinha"

- ⚡ **Capacitores:** Esses componentes armazenam energia e descarregam rapidamente, sendo fundamentais em aplicações que requerem picos de energia, mas devem ser manuseados com cuidado devido ao risco de choque.

<div align="center">
<br>
<img src="./../img/capacitor.png" alt="">
<br>
</div>

- 1º: Capacitor sem polaridade
- 2º e 3º: Capacitores polarizados
- Capacitância do capacitor: quanto de energia ele consegue armazenar. Medido em Farad(F).
- Voltagem máxima escrita no capacitor (ex. do vídeo: 25V), se ultrapassar disso, explode.


<div align="center">
<br>
<img src="./../img/rele.png" alt="">
<br>
</div>



- 🚦 **Transistores:** Eles revolucionaram a eletrônica, substituindo válvulas, e permitem o controle da corrente elétrica, tornando dispositivos mais compactos e eficientes.
- 🔗 **Interconexão de Circuitos:** A interação entre componentes, como o uso de relés e transistores, ilustra como circuitos podem ser controlados eletronicamente, aumentando sua versatilidade.
- 🛠️ **Prática e Teoria:** A combinação de teoria com a prática, como em projetos de circuitos, solidifica o aprendizado e permite a aplicação real do conhecimento adquirido.


#### **Fundamentos da linguagem C/C++:**


#### **Eletrônica Básica:**

#### **Implantação de estrutura de fontes de recursos e base de exercícios no GitHUB**

#### **Tinkercad:**
<br>

### <a name="1-instrucao"></a> Aula 1 - Programação em Arduino e Eletrônica Básica - Instrução


<br>

### <a name="1-ponderada"></a> Aula 1 - Programação em Arduino e Eletrônica Básica - Ponderada