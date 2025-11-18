# 📌 User Story (História de Usuário)

> Uma User Story é uma descrição simples, direta e centrada no usuário sobre algo que ele precisa fazer no sistema.

-  a user story é sempre escrita do **ponto de vista do usuário**, não do sistema nem do desenvolvedor
-  normalmente segue o formato:
      - Como `tipo de usuário`
      - Eu quero `uma ação`
      - Para que `um benefício/objetivo`
 
#### 🎯 Exemplo 
  - **Como** paciente
  - **Eu quero** visualizar meus orçamentos
  - **Para que** eu possa acompanhar meus procedimentos médicos

### 🧪 Como a user story se aplica ao QA?

(1) são ponto de partida para entender o que realmente deve ser entregue
> o QA lê a user story e entende claramente a intenção da funcionalidade, isso evita testes focados apenas na interface e ajuda a testar **valor real**

(2) ajudam a criar critérios de aceitação
> Cada user story deve ter critérios de aceitação, que o QA vai usar como base para escrever casos de teste

**Exemplo:**

`User Story:`

Como paciente, quero visualizar meus orçamentos.

`Critérios de sceitação:`
  - O paciente deve ver apenas os seus orçamentos
  - O sistema deve exibir mensagens quando não houver orçamentos
  - Os dados exibidos devem incluir: nome do procedimento, preço, data, etc

(3) ajudam a encontrar falhas e avistar melhorias antes do desenvolvimento ou durante o desenvolvimento (antes da entrega final)
> Durante refinamento, o QA usa as User Stories para questionar:
  - “E se o paciente não tiver orçamentos?”
  - “E se o paciente tentar acessar o orçamento de outra pessoa?”
  - “Como fica no mobile?”

Isso vai reduzir bugs futuros e garantir a experiência do usuário nas partes vitais do sistema/software. 

------------------

### 🔁 User Story × Requisitos × Regras de Negócio

`Regra de Negócio`

É a regra real do negócio, independente do sistema.

**Exemplo:** Pacientes só podem ver seus próprios orçamentos.

`Requisitos (funcionais e não funcionais)`

São traduções das regras de negócio em comportamentos do sistema.

**Exemplo funcional:** O sistema deve restringir acesso a orçamentos de outros pacientes.

**Exemplo não funcional:** A lista de orçamentos deve carregar em até 2 segundos.

`User Stories`

São narrativas que expressam as necessidades do usuário.

**Exemplo:** Como paciente, quero visualizar meus orçamentos para acompanhar meus procedimentos.

-----
**👉 As User Stories não substituem requisitos e regras de negócio**
> Mas elas ajudam a organizar e apresentar essas informações de forma clara e centrada no usuário

Elas trabalham assim:

#### Regra de Negócio → gera Requisitos → que são agrupados e organizados em User Stories.

Ou seja:

- User Story = necessidade do usuário
- Regras = regras internas da empresa
- Requisitos = como o sistema vai funcionar para atender tudo isso




















