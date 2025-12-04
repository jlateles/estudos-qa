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

------------------

### 4. Mensagens de erro devem ser visíveis + perceptíveis
> Acessibilidade exige mais que só “mostrar a mensagem”.

✔ Requisitos:
  - Deve ter contraste adequado (min. 4.5:1)
  - Deve aparecer sem depender apenas de cor
  - Deve ter texto + símbolo/ícone
  - Deve ser lida automaticamente pelo leitor de tela

Isso é feito usando:
`aria-live="assertive"`
> Ele faz o leitor de tela anunciar a mensagem de erro instantaneamente.

------------
### 5. Mensagens de erro precisam ser anunciadas ao foco

Quando o usuário volta para o campo, o leitor de tela deve dizer:
  - “Campo e-mail, inválido. O e-mail deve ter um formato válido.”

Isso só funciona quando:
  - A mensagem tem `aria-describedby="id-da-mensagem"`
  - O campo tem ID
  - A mensagem tem ID correspondente

**É algo que QA testa inspecionando e usando NVDA ou VoiceOver**
---------------------

### 6. Erros em múltiplos campos devem acompanhar o usuário

Quando há mais de um erro:
  - O foco deve ir para o primeiro campo com erro
  - Um resumo opcional no topo pode existir, mas cada campo ainda precisa da sua própria mensagem

🟧 Erros comuns de acessibilidade
  - Mensagem longe do campo
  - Campo vermelho sem mensagem
  - Mensagem só em cor vermelha (sem texto é inacessível)
  - Mensagem não lida pelo leitor de tela
  - Mensagem aparece apenas após enviar o form
  - Erro genérico (“Há erros no formulário”)
  - Erro que some quando o usuário pressiona TAB
  - O foco não volta para o campo com problema
  - Modal de erro sem `aria-role “dialog”` e não capturando foco

> Cada um desses causa falhas diretas para usuários com deficiência.

🟩 Como QA testa mensagens de erro na prática

✔ Teste padrão
  - Preencha errado
  - Envie o formulário
      - Verifique:
          - posição
          - clareza
          - especificidade
          - contraste
          - leitura pelo leitor de tela
          - foco indo para o campo correto

✔ Teste com teclado
  - Navegue com TAB e SHIFT+TAB
  - Certifique-se de que a mensagem é anunciada
  - Veja se o foco não pula campos com erro

✔ Teste de leitor de tela
  - NVDA → setas / H / F / D
      - Verificar anúncios:
          - campo
          - tipo
          - estado (inválido)
          - mensagem
-------------------------------

## Conslusão 

**Uma mensagem de erro acessível deve:**
  - Aparecer no lugar certo (junto ao campo)
  - Explicar o que aconteceu
  - Explicar como resolver
  - Ter acessibilidade visual (contraste, ícone, não depender apenas de cor)
  - Ser anunciada por leitores de tela
  - Redirecionar o foco corretamente
  - Ser consistente e clara
