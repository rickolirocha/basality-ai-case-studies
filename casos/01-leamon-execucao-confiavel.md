# Leamon — um processo ativo não significa trabalho concluído

**Projeto:** software de coordenação de agentes de IA, em desenvolvimento.  
**Minha atuação:** definição de produto e critérios de aceite, coordenação de implementações assistidas por IA e revisão dos testes.

## Problema

Quando uma tarefa de programação passa para um agente, o trabalho não acaba na resposta do chat. Ainda é preciso saber se ele executou, se produziu o arquivo esperado, se a alteração passou pelos testes e se pode ser aplicada. Uma interrupção também pode deixar registros incompletos ou recursos ainda reservados.

O Leamon nasceu da tentativa de reduzir esse trabalho de acompanhamento sem entregar ao agente autoridade irrestrita para modificar o projeto.

## O que fizemos

Separamos três responsabilidades: o agente executa uma tarefa delimitada; o sistema acompanha estado e evidências; a pessoa aprova mudanças que extrapolam o combinado. Trabalhamos com checkpoints e verificações antes de integrar alterações.

Um problema concreto apareceu na inicialização do processo responsável pela execução: em alguns cenários, o processo já existia, mas ainda não respondia aos comandos de controle. O procedimento anterior podia concluir cedo demais que a inicialização havia falhado.

A correção foi esperar a confirmação do **mesmo processo iniciado**, com um limite de tempo definido — sem tratar a presença do processo como prova de prontidão. Essa alteração teve **18 testes direcionados aprovados** e um ensaio isolado com um processo real no Windows.

Outra investigação reproduziu um processo que deixou uma trava após encerrar. Em teste físico isolado, foi possível reconhecer o proprietário anterior como encerrado e recuperar a execução preservando os registros. Isso **não comprova** que o incidente histórico tenha sido recuperado automaticamente.

## O que levo desse caso

Tentar novamente, reiniciar e declarar sucesso são ações diferentes. Se o sistema não sabe com segurança quem é o dono de um processo ou se uma mudança foi aplicada, ele precisa informar isso antes de continuar.

**Estado:** existem testes e fluxos internos funcionando; a validação do produto como um todo segue em andamento. O caso não representa um lançamento ou garantia geral de recuperação.

[Voltar aos estudos](../README.md)
