### Distributed Transactions with SAGA


## **Coreografia**
A tipografia é uma maneira de coordenar os pontos em que os participantes trocam eventos sem um ponto de controle centralizado. Com a limpeza, cada transação local publica eventos de domínio que disparam transações locais em outros serviços.

**Benefícios**
Bom para fluxos de trabalho simples que exigem poucos participantes e não precisam de uma lógica de coordenação.
Não requer implementação e manutenção de serviço adicionais.
Não introduz um único ponto de falha, pois as responsabilidades são distribuídas entre os participantes do programa.

**Desvantagens**
O fluxo de trabalho pode se tornar confuso ao adicionar novas etapas, pois é difícil acompanhar quais participantes do programa escutam quais comandos.
Há um risco de dependência cíclica entre os participantes do programa porque eles precisam consumir os comandos uns dos outros.
O teste de integração é difícil porque todos os serviços devem estar em execução para simular uma transação.

<br>

## **Orquestração**
A orquestração é uma maneira de coordenar as coordenadas em que um controlador centralizado informa aos participantes quais transações locais executar. O orquestrador de orquestrador trata todas as transações e informa aos participantes qual operação executar com base em eventos. O orquestrador executa solicitações, armazena e interpreta os estados de cada tarefa e lida com a recuperação de falha com transações de compensação.

**Benefícios**
Bom para fluxos de trabalho complexos que envolvem muitos participantes ou novos participantes adicionados ao longo do tempo.
Adequado quando há controle sobre cada participante no processo e controle sobre o fluxo de atividades.
Não introduz dependências cíclicas, pois o orquestrador depende dos participantes do programa.
Os participantes não precisam saber mais sobre comandos para outros participantes. A separação clara de preocupações simplifica a lógica de negócios.


**Desvantagens**
A complexidade de design adicional requer uma implementação de uma lógica de coordenação.
Há um ponto adicional de falha, porque o orquestrador gerencia o fluxo de trabalho completo.
