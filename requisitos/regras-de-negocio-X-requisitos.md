# Regras de Negócio x Requisitos

## 🔵 Requisitos
é o que os nossos usuários nos pedem, normalmente dividimos entre  funcionais e não-funcionais. Então, é uma necessidade do sistema, uma função ou comportamento que o software precisa ter para implementar uma regra de negócio ou para melhorar a experiência do usuário.

**exemplos:** 
- funcionais: “quero que o programa seja capaz de faturar uma venda” (funcionais é **o que** o sistema deve fazer)
- não-funcionais: “quero que a venda seja faturada em até 5 segundos” (não-funcionais é **como** o sistema deve ser, não o que ele faz - define velocidade, segurança, usabilidade, etc)

> Requisitos são traduções das regras de negócio para dentro do sistema.

--- 
## 🟢 Regra de Negócio
é tudo aquilo que esta inerentemente ligado ao negócio que estamos fazendo.  É algo que existe independentemente do sistema e da tecnologia usada. São diretrizes, condições e restrições que definem como o negócio deve funcionar. 

**exemplos:**
  - “Um paciente só pode ver seus próprios orçamentos.”
  - “Procedimentos de alta complexidade precisam de aprovação médica.”

> Essas regras explicam como o negócio funciona.

---

## Relação entre os 2 (requisitos & regras de negócio): 
> A regra de negócio é o que deve acontecer.
> O requisito é como o sistema vai garantir que isso aconteça.

`Regra de Negócio:` Só Administradores ou recepcionistas podem criar orçamentos.

`Requisito correspondente:`
  - O sistema deve permitir acesso ao módulo de criação de orçamento apenas para usuários com perfil Admin ou Recepção.
  - O sistema deve exibir mensagem de erro se um usuário sem permissão tentar criar um orçamento.

 A regra existe fora do sistema.
 O requisito é como o sistema implementa isso.
