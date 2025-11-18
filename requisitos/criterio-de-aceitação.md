# Critérios de Aceitação (CA) 
 ✅ são condições específicas e objetivas que definem quando uma **User Story** é considerada concluída e aceitável.

> Critérios de Aceitação são as regras de “ok, isso está pronto” de uma User Story
>
> São verificações que o QA usa para validar que a funcionalidade está funcionando como esperado

## 🎯 Para que servem?
- Validar se a funcionalidade está correta  
- Alinhar QA, dev e negócio  
- Evitar interpretações diferentes  
- Garantir que a entrega está completa  
-----
### 🧠 Por que eles são importantes para o QA?

- Base direta para criar testes
> Cada critério vira um cenário de teste.

- Evitam interpretação diferente entre times
> Sem CA, cada pessoa entende a User Story de um jeito.

- Evitam entregas incompletas
> O QA só aprova a entrega se todos os critérios forem atendidos.

- Ajudam a identificar cenários negativos
> Eles permitem prever casos de erro, faltas de dados, acessos indevidos etc
----
### 📌 Formato comum dos Critérios de Aceitação
A forma mais usada é Gherkin, com:
  - Given (Dado)
  - When (Quando)
  - Then (Então)

*Exemplo:*

Dado (Given) que sou um paciente logado

Quando (When) acesso a aba "Orçamentos"

Então (Then) devo visualizar somente os meus orçamentos
