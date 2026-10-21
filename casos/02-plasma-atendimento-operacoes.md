# Plasma — por que testamos uma resposta privada antes do envio automático

**Projeto:** automação de atendimento e operações para e-commerce, em desenvolvimento.  
**Minha atuação:** desenho e coordenação da frente de atendimento, especificação de testes e revisão das integrações.

## Problema

Um atendimento automatizado pode consultar o pedido certo e ainda assim causar problema: repetir uma mensagem, usar uma atualização antiga ou responder enquanto um atendente humano assume a conversa.

No Plasma, estamos conectando dados de pedidos, comunicação e atendimento por etapas. A primeira preocupação não é fazer o bot responder a tudo, mas saber **qual informação está confirmada e quem pode agir sobre ela**.

## O teste que mudou a decisão

Queríamos evitar que o bot enviasse uma resposta depois de a conversa ter sido assumida por uma pessoa. No ensaio com **Chatwoot e Evolution em ambiente isolado**, vimos que a atribuição ao atendente não impedia atomicamente uma nova mensagem pública do bot. Uma verificação feita um instante antes do envio não eliminava a corrida.

Em vez de adicionar imediatamente outra camada de controle, testamos o que o Chatwoot já oferece: **notas privadas**. A resposta sugerida foi registrada para o atendente, sem produzir mensagem pública no canal externo.

Para aquela etapa, mantivemos a IA como apoio ao atendente. O ensaio validou o registro interno da sugestão; o envio autônomo ao cliente continua sem liberação.

## Outros testes

Uma sequência de **oito cenários integrados simulados** verificou, entre outras coisas, a manutenção da identidade do pedido, eventos repetidos, atualizações fora de ordem, consulta a dados persistidos e separação entre respostas e notificações.

Os testes ajudaram a separar três fatos que parecem iguais, mas não são: a ação foi tentada; o serviço aceitou; a mensagem foi entregue. Em notificações, respostas desconhecidas não devem autorizar reenvio automático sem nova evidência.

Esse teste mudou a ordem do trabalho: antes de automatizar o envio, precisamos demonstrar uma forma segura de lidar com a intervenção humana.

**Estado:** testes simulados e provas nativas isoladas; envio autônomo ao cliente e integração completa em produção ainda não validados.

[Voltar aos estudos](../README.md)
