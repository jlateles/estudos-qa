## Critérios de Aceitação (CA) x Regras de Negócios (RDN) x User Story (US) x Requisitos (REQ)
> exemplo prático dos 4 tópicos acima

### User Story
**Como** paciente  
**Eu quero** visualizar meus orçamentos  
**Para que** eu possa acompanhar meus procedimentos médicos  

### Critérios de Aceitação
1. O paciente deve visualizar apenas os orçamentos vinculados ao seu CPF  
2. Se o paciente não tiver orçamentos, deve exibir: **“Nenhum orçamento encontrado”**  
3. Cada orçamento deve apresentar procedimento, valor, status, data, etc  
4. A página deve carregar a listagem em até 2 segundos  
---
## 🔁 Relação com Regras de Negócio, Requisitos e User Stories

**Regra de Negócio**
> Define como o negócio funciona.  
Exemplo: “Pacientes só podem ver orçamentos criados para eles.”

**Requisito Funcional**
> Descreve o comportamento do sistema.  
Exemplo: “O sistema deve impedir acesso a orçamentos de terceiros.”

**Requisito Não Funcional**
> Descreve características do sistema.  
Exemplo: “A página deve carregar em até 2 segundos.”

**User Story**
> Descreve a necessidade do usuário.  
Exemplo: “Como paciente, quero visualizar meus orçamentos.”

**Critérios de Aceitação**
> Definem quando a User Story está pronta.  
Exemplo: “Mostrar apenas orçamentos do paciente”, “mensagem de vazio”, etc.
---

## Resumo
- **Regra de Negócio** = o negócio precisa disso  
- **Requisito** = o sistema deve fazer isso  
- **User Story** = o usuário precisa/quer disso  
- **Critérios de Aceitação** = consideramos pronto quando isso estiver funcionando  
