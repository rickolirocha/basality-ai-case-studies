# Estudos de caso — Basality

Registros de problemas que investiguei, decisões tomadas e testes realizados na construção de sistemas com IA e automação. São projetos em diferentes estágios, não demonstrações de produtos concluídos.

## Projetos

### [Leamon — quando um agente termina, como saber se o trabalho terminou?](casos/01-leamon-execucao-confiavel.md)

O projeto trabalha com execução de agentes, retomada e aprovação de mudanças. O caso mostra testes que diferenciam um processo ativo de um sistema pronto e investiga recuperação após falhas.

### [Plasma — quando o humano assume, o bot pode continuar respondendo?](casos/02-plasma-atendimento-operacoes.md)

Testamos a integração entre operação de pedidos e atendimento. Um problema encontrado no envio concorrente levou a uma alternativa com notas privadas para revisão humana. Também há testes de repetição de eventos e estados de pedidos.

### [Basality — como decidir se um processo precisa mesmo de IA?](casos/03-basality-contexto-metodo.md)

Como organizo diagnóstico, contexto e experimentos antes de escolher ferramentas, inclusive quando a melhor solução é uma regra simples ou uma etapa manual.

### [MeuAmiguinho — o que aprendi operando um e-commerce](casos/04-meuamiguinho-ecommerce.md)

Experiência anterior em crescimento, aquisição e atendimento. O caso explica como ela influencia as decisões que tomo hoje ao desenhar automações.

## Como interpretar os resultados

Os testes mencionados são específicos: uma simulação aprovada não comprova funcionamento em produção, e uma integração exercitada isoladamente não demonstra uma operação completa. Quando algo ainda não foi validado, indico o limite no próprio relato.

[Como trato evidências e números](CRITERIOS_DE_EVIDENCIA.md)

---

**Por [Ricardo Oli Rocha](https://github.com/rickolirocha) · [Basality](https://basality.com.br/)**
