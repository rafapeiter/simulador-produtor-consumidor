# Simulador Produtor-Consumidor

Este projeto implementa, em uma interface web interativa, o problema clássico de sincronização **Produtor-Consumidor** da disciplina de Sistemas Operacionais.

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

## Funcionalidades da interface

- Botão para iniciar/parar a simulação;
- Visualização gráfica das posições do buffer;
- Atualização em tempo real da quantidade de itens no buffer;
- Logs separados para ações do produtor e do consumidor;
- Destaque visual para estados críticos (cheio/vazio).

## Tecnologias utilizadas

- **HTML5**
- **CSS3**
- **JavaScript (Vanilla)**
- **Bootstrap 5** (via CDN)

## Como executar

Como o projeto é estático, não há dependências para instalar.

1. Clone o repositório:

	 ```bash
	 git clone https://github.com/rafapeiter/simulador-produtor-consumidor.git
	 cd simulador-produtor-consumidor
	 ```

2. Abra o arquivo `index.html` no navegador.

Opcionalmente, você pode usar um servidor local simples:

```bash
python3 -m http.server 8000
```

Depois acesse `http://localhost:8000`.

## Objetivo educacional

Este simulador foi desenvolvido para facilitar o entendimento de:

- sincronização entre processos/threads;
- funcionamento de buffer circular;
- cenários de bloqueio por recurso indisponível;
- impacto de taxas diferentes de produção e consumo.