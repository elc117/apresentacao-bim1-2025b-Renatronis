# Apresentação de exercício
## Vídeo do código em execução



https://github.com/user-attachments/assets/9665c954-82c6-4f40-9163-42f200c1f811

## Análise dos trechos do código
### Parte 1- Imports
  
<img width="298" height="123" alt="image" src="https://github.com/user-attachments/assets/3545de6c-849e-4b8e-890f-b9735b5a7902" />

Nesse primeiro trecho podemos notar a presença do "import" que remete ao "#include" do C e sim, ele faz basicamente isso, importa bibliotecas.


### Parte 2- Vectors

<img width="537" height="255" alt="image" src="https://github.com/user-attachments/assets/30f3ee9f-9f48-406c-9865-88c635d8d8a0" />

Nesse trecho, sem termos amplo conhecimento da linguagem, podemos notar o cálculo de coordenas e alguns artifícios novos, por exemplo a presença de uma nova função o **fromIntegral**, que faz basicamente o que o nome enuncia, converte um valor para integral.
Ainda temos o **where** que serve para criar definições locais (variáveis ou funções auxiliares) que só valem dentro daquela função. O **@** que permite dar nome ao valor inteiro ao mesmo tempo em que você decompõe ele em partes e também o **atan2** que calcula o ângulo de uma coordenada no plano cartesiano.

### Parte 3- Map

<img width="642" height="633" alt="image" src="https://github.com/user-attachments/assets/2a908774-0a3b-4c24-b9f9-41d2d019fdad" />

Aqui podemos supor, com base no vídeo do código em execução, que tem relação com a criação das estruturas das paredes do jogo. Também notamos algo novo, o **Type**, ele serve para dar um nome alternativo para um **Int**, por exemplo. Há funções novas como a **concat** que pega uma lista de listas e transforma em uma lista única e 
**zipWith** que combina duas listas elemento a elemento, aplicando uma função a cada par e, por fim, o  **read** que pega uma string e transforma em um valor de outro tipo.


### Parte 4- Game State

<img width="315" height="194" alt="image" src="https://github.com/user-attachments/assets/7f43e4ad-922f-4812-8138-ace7a9ea4b56" />

Na seção Game State temos o que em C chamamos de struct, ela esta diretamente ligada ao estado do jogo. Podemos supor isso pelos nomes dados dentro dessa estrutura. O **State** faz um papel fundamental em define o estado completo do jogo em um único valor. 
Ele reúne todas as informações necessárias para que o jogo funcione corretamente.
O **deriving** permite que o compilador gere automaticamente implementações de certas classes para o tipo definido, no nosso caso o deriving (Show) faz com que o State possa ser imprimido no console.


### Parte 5- Event Handling

<img width="670" height="433" alt="image" src="https://github.com/user-attachments/assets/dbb370c1-ef05-4ce0-974b-0426929c5189" />

Para contextualizar, nesse jogo você se move através das teclas e do movimento do mouse, sabendo disso e prestando atenção no comentário do código "EVENT HANDLING", pode-se deduzir que esse trecho lida com os movimentos do jogador durante o jogo e atualiza a sua posição
durante a experiência. Ainda temos um novo artifício da linguagem presente, o **if** que ainda não tinhamos visto.


### Parte 6- Ray Casting

<img width="647" height="745" alt="image" src="https://github.com/user-attachments/assets/8f06b273-ca6c-4956-b4f1-faa11cf54904" />

<img width="551" height="290" alt="image" src="https://github.com/user-attachments/assets/9b984656-eacf-406e-95d4-616d78a3c451" />

Nesse trecho de código fica mais difícil para quem não tem experiência com a linguagem compreender o que está acontecendo. Mas prestando atenção em uma função específica chamada **collision** e também pelos cálculos de coordenadas podemos relacionarcom a colisão do jogador com os objetos do mapa. Podemos notar também a função **floor** que serve para arredondar um número para baixo e **abs** que retorna o valor absoluto de um número.


### Parte 7- Rendering

<img width="684" height="700" alt="image" src="https://github.com/user-attachments/assets/15e39989-0047-4961-a93e-7fe997164c11" />

<img width="678" height="597" alt="image" src="https://github.com/user-attachments/assets/7ada6015-85b2-4110-8e1b-d576873265bf" />

Em Rendering é visto uma manipulação das dimensões da tela, das cores das paredes, do desenho do minimapa e da posição do jogador. Podemos notar isso atraves dos nomes das funções que remetem a manipulação de tamanhos, cores, etc. Além das cooredenadas x e y para calcular a posição dos objetos.
Também notamos uma outra função nativa de haskell a **uncurry**  que converte uma função que recebe dois argumentos separados em uma função que recebe uma tupla.


### Parte 8- Main

<img width="343" height="280" alt="image" src="https://github.com/user-attachments/assets/65289e75-d64d-4ad9-a173-627137829739" />

Com base na linguaguem C, podemos supor que na seção Main o jogo é inicizalizado com a passagem de valores para o **State** que foi definido no código anteriormente. Aqui, para enterder melhor como funciona a inicilização, 
deveriamos saber que "main :: IO ()" é uma ação de entrada/saída (IO), padrão em Haskell para programas que interagem com o mundo externo.

## Conclusão
Após analisar o código com atenção, pude concluir que para quem arrecém iniciou sua joranda de aprendizado em Haskell, não é uma tarefa fácil decifrar o que o código faz de maneira mais detalhada, muito por causa da sintaxe que o iniciante não está acostumado, mas principalmente pelas diversas funções não abordadas ainda na linguagem. 
Porém, mesmo sem ter os conhecimentos necessários para destrinxar o código por completo, analisa-lo foi muito útil para estimular o pensamento, aprender novas utilidades para o Haskell e desenvolver e adquirir novos conhecimentos.

## Referências

DU BOIS, André Rauber. Programação Funcional com a Linguagem Haskell. Disponível em: https://www.inf.ufpr.br/andrey/ci062/ProgramacaoHaskell.pdf. Acesso em: 20 ago. 2025.

CodeWorld Reference: https://code.world/haskell.
