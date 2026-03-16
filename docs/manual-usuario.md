# Manual do Usuário — Cozinha Inteligente

Este documento apresenta um guia básico de utilização dos sistemas desenvolvidos para automação e monitoramento em ambientes de cozinha. As soluções foram projetadas para aumentar a segurança, melhorar o controle operacional e facilitar o monitoramento de processos críticos.

---

# 1. Sistema de Controle de Tempo para Fritadeira

## Descrição do sistema
O sistema de controle de fritadeira é um dispositivo embarcado projetado para automatizar o tempo de funcionamento da fritadeira elétrica, garantindo maior padronização no preparo dos alimentos e reduzindo a necessidade de monitoramento constante pelo operador. 

## Componentes principais

- Placa de controle embarcada (BitDogLab / RP2040)
- Potenciômetro para ajuste de tempo
- Relé de acionamento da fritadeira
- Dispositivo de alerta sonoro

## Como utilizar

### 1. Ligar o sistema
- Conecte o sistema à energia.
- O dispositivo inicializará automaticamente.

### 2. Definir o tempo de preparo
- Ajuste o **potenciômetro** para selecionar o tempo desejado de funcionamento da fritadeira.

### 3. Iniciar o processo
- Após o ajuste do tempo, o sistema acionará o relé, ligando a fritadeira.

### 4. Aguardar o término do ciclo
- A fritadeira permanecerá ligada pelo tempo definido.

### 5. Receber o alerta
- Ao final do tempo programado, o sistema desligará a fritadeira e emitirá um alerta, indicando que o preparo foi concluído.

## Observações

- Ajuste o tempo antes de iniciar o preparo.
- O sistema permite que o operador execute outras tarefas enquanto o alimento está sendo preparado.

---

# 2. Sistema de Monitoramento de Vazamento de Gás

## Descrição do sistema

O sistema de monitoramento de gás foi desenvolvido para detectar vazamentos de gases inflamáveis no ambiente da cozinha, aumentando a segurança operacional. :contentReference[oaicite:2]{index=2}

## Componentes principais

- Placa de controle embarcada (BitDogLab / RP2040)
- Sensor de gás MQ
- Mecanismo de alerta

## Como utilizar

### 1. Ligar o sistema
- Conecte o dispositivo à alimentação elétrica.
- O sensor iniciará o processo de leitura do ambiente.

### 2. Monitoramento automático
- O sistema realiza leituras contínuas da concentração de gás no ambiente.

### 3. Detecção de vazamento
- Caso a concentração de gás ultrapasse o limite de segurança programado, o sistema acionará automaticamente um alerta.

### 4. Resposta ao alerta
Ao ouvir o alerta:

- Verifique imediatamente possíveis vazamentos.
- Feche o registro de gás, se necessário.
- Ventile o ambiente.

## Observações

- O sistema funciona continuamente após ser ligado.
- Recomenda-se manter o sensor instalado próximo à área de uso do gás.

---

# 3. Sistema de Monitoramento do Peso do Botijão de Gás

## Descrição do sistema

O sistema de monitoramento de peso permite acompanhar o nível de gás presente no botijão, ajudando a prever quando o gás está próximo de acabar e evitando interrupções nas atividades da cozinha. :contentReference[oaicite:3]{index=3}

## Componentes principais

- Base com células de carga
- Módulo HX711
- Microcontrolador (RP2040)
- Sistema de monitoramento web

## Como utilizar

### 1. Posicionar o botijão
- Coloque o botijão de gás sobre a base da balança do sistema.

### 2. Inicialização do sistema
- Ao ligar o dispositivo, o sistema inicia automaticamente a leitura do peso.

### 3. Monitoramento do peso
- O peso do botijão será medido continuamente pelas células de carga.

### 4. Visualização das informações
- Os dados coletados podem ser visualizados no painel web de monitoramento, que apresenta informações sobre o peso atual e o estado do sistema.

### 5. Identificação de nível crítico
- Quando o peso do botijão se aproxima de um limite mínimo, o sistema pode indicar a necessidade de reposição do gás.

## Observações

- Pequenos atrasos na atualização do painel podem ocorrer devido à transmissão dos dados, o que não compromete o funcionamento do sistema.
- O monitoramento permite realizar a reposição do botijão de forma preventiva.

---
