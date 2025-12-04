# Identificação de erros na acessibilidade

### 🌟 Qual é a premissa central na identificação de um erro? 

> O usuário precisa saber:
>   - Onde (exatamente) ocorreu o erro
>   - O que (exatamente) está errado
>   - Como (exatamente) resolver

Isso vale para qualquer usuário — mas para **acessibilidade**, **vale dobrado**.
  - Porque pessoas com baixa visão, usuários de leitores de tela, quem usa lupa ou navega por teclado dependem totalmente da *clareza*, *visibilidade* e *localização correta* da mensagem.

-----

### 🟣 Por que isso é crítico para acessibilidade?
  - Uma mensagem vaga (ex.: “Erro no campo”)
  - Uma mensagem longe do campo
  - Um aviso só em cor (vermelho)
  - Um texto não lido pelo leitor de tela
  - Uma mensagem genérica (“Algo deu errado”)

**Tudo isso cria barreiras que impedem o usuário de continuar**

> E para quem tem deficiência visual ou cognitiva, isso significa:
  - Frustração
  - Ação impossibilitada
  - Erro repetitivo
  - Abandono do processo

**Erros bem comunicados não são um detalhe, são essenciais para tornar o sistema usável**

--------------

### 1. O usuário precisa saber onde foi o erro
> É obrigatório que a mensagem esteja junto ao campo com problema, nunca isolada.

✔ Boas práticas:
  - A mensagem aparece imediatamente abaixo ou acima do campo
  - O campo recebe estilo destacando o erro (borda, outline)
  - Há um ícone de alerta visível
  - O leitor de tela anuncia o erro quando o foco entra no campo

❌ Erros comuns:
  - Mensagem aparece no topo da tela (“Preencha corretamente os campos abaixo”) => inacessível
  - Somente borda vermelha (cor não pode ser o único indicador!)
  - Mensagem aparece só ao enviar o formulário

### 2. O usuário precisa saber o que está errado
> A mensagem precisa ser específica e completa

✔ Boas práticas:
  - “O e-mail deve ter um formato válido”
  - “O CEP precisa ter 8 dígitos”
  - “Os e-mails precisam ser iguais”
  - “Informe apenas letras no campo Nome”
  - “A data não pode ser maior que a data atual”

❌ Erros comuns:
  - “Campo inválido”
  - “Erro nos dados”
  - “Informe corretamente”

*Mensagens específicas reduzem erros e ajudam muito quem tem dificuldades cognitivas ou interpretações diferentes*

### 3. O usuário precisa saber como resolver
> Toda mensagem de erro deve ensinar o que fazer.

✔ Boas práticas:
  - “Digite um CEP com 8 dígitos”
  - “Use apenas números no campo x”
  - “A senha precisa ter pelo menos 8 caracteres”
  - “Selecione pelo menos um procedimento/item antes de avançar” 

**Uma mensagem sem instrução deixa o usuário perdido, mesmo sabendo onde está o erro.**
