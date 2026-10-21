# Basality — como escolher a menor intervenção que vale testar

**Tema:** método de trabalho usado em diagnósticos e projetos de automação.  
**Estado:** abordagem em uso e evolução, sem atribuição de ganhos financeiros a clientes neste relato.

## A pergunta inicial

Quando alguém descreve um processo lento, é tentador responder com um agente, uma plataforma ou uma integração. Tento começar de outro ponto: o que a pessoa precisa conseguir fazer, o que impede isso hoje e como saberemos que melhorou?

Chamo de **arquitetura mínima suficiente** a decisão de implementar apenas o que o problema exige naquele momento. Não é um framework próprio nem uma regra de que sistemas complexos são sempre ruins.

## Como aplico

1. **Descrevo o trabalho atual.** Quem recebe a informação, quem decide, quais ferramentas usa e onde acontece retrabalho.
2. **Defino o resultado e as restrições.** O que seria uma melhoria observável? O que não pode dar errado? Que dados e permissões estão disponíveis?
3. **Testo a menor mudança plausível.** Pode ser um checklist, uma regra, uma integração ou um agente. Só acrescento uma peça quando há uma razão identificável.

Também procuro deixar objetivos, decisões e resultados registrados em arquivos legíveis. Isso facilita retomar trabalho com diferentes agentes sem depender de alguém reconstruir todo o contexto a cada conversa.

## Exemplo prático

No Leamon, um processo recém-iniciado podia demorar a responder aos comandos de controle. Em vez de criar outro serviço de supervisão, ajustamos a espera pelo processo correto e definimos um prazo máximo. A solução teve testes direcionados e uma prova isolada no Windows, como explico no [caso Leamon](01-leamon-execucao-confiavel.md).

É uma correção específica, não uma medição de produtividade ou redução de custo em clientes.

## Referências

Minha organização de contexto se inspira especialmente na [Interpretable Context Methodology (ICM)](https://arxiv.org/abs/2603.16021), de Jake Van Clief e David McDermott. Também acompanho trabalhos sobre [engenharia de contexto da Anthropic](https://www.anthropic.com/research/effective-context-engineering-for-ai-agents), [harnesses da OpenAI](https://openai.com/index/harness-engineering/) e o [Open Knowledge Format, do Google Cloud](https://github.com/GoogleCloudPlatform/open-knowledge-format). São referências de estudo, não certificações ou validações externas do meu método.

[Voltar aos estudos](../README.md)
