# Simulador Produtor-Consumidor

Este projeto implementa, em uma interface web interativa, o problema clássico de sincronização **Produtor-Consumidor** da disciplina de Sistemas Operacionais.

O projeto foi criado como material de apoio para a disciplina de Programação Paralela e Distribuída, com o objetivo de facilitar o entendimento prático.

## Problema que o projeto resolve

No problema Produtor-Consumidor, dois processos compartilham um buffer limitado:

- **Produtor**: gera itens e tenta inseri-los no buffer;
- **Consumidor**: remove itens do buffer para processá-los;
- **Buffer limitado**: se estiver cheio, o produtor deve aguardar; se estiver vazio, o consumidor deve aguardar.

O simulador demonstra visualmente esses cenários de forma didática, incluindo os estados de espera quando há contenção de recursos.

## Como a simulação funciona

- Buffer circular com tamanho fixo de **5 posições**;
- Ponteiros **IN** (próxima posição de escrita) e **OUT** (próxima posição de leitura);
- Contador de itens para controle do estado do buffer;
- Loops assíncronos de produção e consumo usando `setTimeout`;
- Velocidades configuráveis para produtor e consumidor:
	- Aleatória
	- Rápida (0,5s)
	- Lenta (2,0s)

Quando o buffer está:

- **Cheio**: o produtor entra em espera;
- **Vazio**: o consumidor entra em espera.

Esses eventos são exibidos em dois terminais de log (produtor e consumidor).

## Tecnologias utilizadas

- **HTML5**
- **CSS3**
- **JavaScript (Vanilla)**
- **Bootstrap 5** (via CDN)

## Como usar

Você pode acessar a aplicação diretamente pelo link:

- https://simulador-produtor-consumidor.vercel.app/

Passos rápidos:

1. Abra o link no navegador.
2. Defina a velocidade do **Produtor** e do **Consumidor**.
3. Clique em **Iniciar Simulação**.
4. Acompanhe o buffer, os ponteiros (`IN`/`OUT`) e os valores dos semáforos em tempo real.
5. Use **Parar Simulação** para pausar a execução.
