# 🟣 acessibilidade de conteúdo

A acessibilidade de conteúdo trata de como a informação é apresentada, compreendida e acionada pelo usuário, garantindo que todas as pessoas — incluindo quem possui limitações motoras, visuais, cognitivas ou usa tecnologias assistivas consigam:
  - entender o que está na interface
  - interagir com os elementos
  - navegar sem esforço
  - saber para onde um botão ou link as levará
  - executar ações com clareza e segurança

> Não é só sobre “visualizar” uma tela, mas sobre entender e conseguir agir dentro dela.

### 🎯 Por que testar acessibilidade de conteúdo?

Pois o conteúdo mal formatado (links confusos, botões pequenos, textos pouco claros, ações sem contexto) cria barreiras reais, especialmente para:
  - pessoas com mobilidade reduzida
  - usuários com baixa visão
  - quem usa leitor de tela
  - quem navega apenas por teclado
  - quem usa celular com somente uma mão
  - idosos ou usuários com dificuldade de compreensão
  - pessoas com daltonismo ou problemas de percepção

Quando o conteúdo não é acessível, a aplicação se torna:
    - difícil de usar, confusa, cansativa, insegura (o usuário pode acionar algo errado ou algo que não queira) e excludente.

### 🔍 Qual é o impacto no projeto/aplicação?

✔ Melhora a usabilidade para todos
> Acessibilidade não é só para pessoas com deficiência — melhora a experiência para todo mundo

✔ Evita erros e desistência
> Usuários abandonam formulários e fluxos quando não conseguem entender o que fazer ou não conseguem clicar em algo

✔ Reduz retrabalho e suporte
> Interfaces mais claras = menos chamados, dúvidas e correções

✔ A aplicação fica mais profissional
> Textos claros, ações bem definidas e links descritivos deixam a interface mais confiável

✔ Atende leis e normas (Lei Brasileira de Inclusão, WCAG)
> Muitas empresas exigem conformidade com acessibilidade, principalmente em produtos públicos ou de saúde

### Acessibilidade de conteúdo x acessibilidade visual x acessibilidade estrutural
| Tipo                                          | Foca em             | Exemplos                                                                        |
| --------------------------------------------- | ------------------- | ------------------------------------------------------------------------------- |
| **Acessibilidade visual**                     | Ver/Perceber        | Contraste, legibilidade, tamanhos, cores                                        |
| **Acessibilidade estrutural**                 | Navegar             | Semântica, navegação por teclado, ordem de foco                                 |
| **Acessibilidade de conteúdo**                | **Entender e agir** | Textos claros, links descritivos, botões acionáveis, boa área de clique, instruções |

👉 Visual = ver
👉 Estrutural = chegar/navegar
👉 Conteúdo = entender e executar a ação

-----------------

### Exemplos práticos 

#### 🟦 1. Gestos de acionamento
(área clicável, botões, precisão de toque)

> Garantem que qualquer pessoa consiga acionar um botão, link ou ícone sem esforço e sem erros

📏 Tamanho mínimo da área clicável

Recomendação WCAG: 44px x 44px
Mesmo se o ícone for menor, a área tocável precisa ter esse tamanho.

👀 O que QA valida?
  - Botões muito pequenos
  - Ícones com área clicável insuficiente (menu, fechar modal, carrinho)
  - Opções muito próximas umas das outras
  - Cards onde somente o texto é clicável (em vez do card inteiro)
  - Campos de formulário difíceis de selecionar no mobile

❌ Erro muito comum: 

Ícone de “X” no modal com 16px e sem padding = impossível clicar no celular

✔ Solução: 

Ícone pequeno, mas área clicável ampliada com padding (chegando aos 44px)

#### 🟦 2. Finalidade dos links e ações

(clareza sobre para onde o usuário vai ou o que acontecerá)

O usuário precisa entender claramente o propósito do link ou ação, inclusive quem:
  - usa leitor de tela
  - depende de navegação por teclado
  - tem dificuldades cognitivas
  - tem leitura reduzida
  - está em um fluxo crítico (saúde, orçamento, formulário)

❌ Problema: “clique aqui”, “ver mais”, “saiba mais”, entre outros
> Esses textos não dizem NADA sobre o destino que a aplicação levará o usuário

Para leitores de tela piora ainda mais:
Ele lê: "link: ver mais", "link: ver mais", "link: ver mais" → sem contexto.

✔ O que QA valida?
  - O propósito do link é claro mesmo isolado
  - Links iguais levam para destinos iguais
  - Links diferentes têm descrições diferentes
  - Botões genéricos (continuar, avançar) deixam claro a próxima etapa
  - Ícones sem texto têm aria-label descritivo

✔ Exemplos corretos: 
  - “Ver mais sobre Consultas Dermatológicas”
  - “Acessar meus orçamentos de procedimentos”
  - “Editar informações do paciente” (para ícone de lápis)
---------------------

### Exemplo na interface do projeto base 

