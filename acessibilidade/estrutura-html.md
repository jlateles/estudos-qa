## 🟪 acessibilidade estrutural
> a parte da acessibilidade que garante que a página/tela seja organizada, entendida e navegada de forma coerente, mesmo sem usar a visão

Isso inclui: 
  - estrutura do HTML5 (tags corretas)
  - aria roles
  - hierarquia de títulos (h1, h2, h3, etc)
  - ordem de tabulação (TAB, SHIFT+TAB)
  - ordem lógica do conteúdo
  - landmark regions (nav, main, footer)
  - comportamento de modais e componentes interativos
  - foco visível e rastreável

Um usuário de leitor de tela muitas vezes não vê nada, ele apenas “escuta” a estrutura da página. Se essa estrutura estiver errada, a pessoa fica perdida.

### 🎯 Por que isso importa para QA?

Porque falhas de estrutura quebram totalmente:
  - navegação por teclado
  - uso de leitores de tela
  - a lógica de fluxo da aplicação
  - a experiência de modais, menus, formulários e tabelas
  - o entendimento sobre o conteúdo da página
  - aplicações de saúde, e-commerce, bancos e gov têm alto impacto se esse tipo de acessibilidade falha — e o QA trabalha justamente testando sistemas sensíveis, garantindo que vão cumprir o papel que é esperado.

### 🟦 Semântica HTML5, a base de tudo

> Semântica é usar as tags corretas para o que elas significam

✔ Exemplos de bons usos:

  - `<header>` = cabeçalho
  - `<nav>` = navegação
  - `<main>` = conteúdo principal
  - `<section>` = seções
  - `<article>` = artigos, conteúdo independente
  - `<aside>` = conteúdo lateral
  - `<footer>` = rodapé

#### ❌ Erro comum:
Toda a página feita com `<div>` e `<span>` sem significado => leitores de tela não entendem nada

##### Como QA testa:
  -  Abra DevTools e verificar se há main, nav, header, footer
  -  Teste no leitor de tela: ele deve anunciar “Região principal”, “Navegação”, “Rodapé”
-----

### 🟦 2.Hierarquia de títulos (H1, H2, H3…)
> considere que headings como o índice da página para usuários cegos/com baixa visão 

Regras importantes:
  - deve existir um único H1
  - os títulos devem seguir ordem lógica (h1 > h2 > h3)
  - não pode pular níveis do nada (h1 → h4 sem contexto)

##### Como QA testa:
  - use extensões como HeadingsMap, Axe Devtools ou somente inspecione
  - no leitor de tela, navegue por headings: ele precisa fazer sentido.

------

### 🟦 3. Landmarks 
> leitores usam para “pular para a parte certa”

Landmarks são regiões da página, como:
  - main
  - nav
  - header
  - footer
  - form
  - aside
  - section

O leitor de tela permite o usuário “pular” direto para um landmark

##### Como QA testa:
  - No NVDA, pressione D para ir para landmarks
  - Ele deve anunciar: “Região de navegação”, “Main landmark”, etc
  - Se nada for anunciado é porque a página não tem estrutura.

----- 
### 🟦 4. Ordem de foco (TAB Order)

usuários de teclado e leitores de tela navegam com:
  - TAB (próximo elemento)
  - SHIFT + TAB (voltar)
  - SETAS (leitores de tela)
  - ENTER / SPACE (executar ação)

✔ O foco deve seguir uma ordem lógica:
  - Exemplo esperado:
      - header
      - menu
      - conteúdo principal
      - formulários
      - botões de ação
      - footer

❌ Erros comuns encontrados em testes:
  - foco “salta” para lugares aleatórios
  - foco entra dentro de componentes invisíveis
  - o usuário fica preso dentro de um card/menu
  - foco some (desaparece visualmente)
  - elementos não são focáveis quando deveriam (ex.: botão feito com <div>)
  - elementos “tabáveis” sem necessidade (ex.: <span tabIndex="0"> sem motivo)

##### Como QA testa:
  - pressionar TAB várias vezes e confirmar:
      - a ordem segue fluxo visual
      - nada é pulado
      - nada entra em loops
      - o foco sempre é visível
---------------
### 🟦 5. Foco Visível 
> Mesmo se a acessibilidade visual for excelente, sem foco visível a navegação por teclado fica impossível

O que testar:
  - Quando TAB é pressionado, existe outline, borda ou destaque claro?
  - No dark mode, o foco também aparece?
  - O foco não fica escondido atrás de elementos flutuantes?
  - O foco entra dentro de modais?

---------------
### 🟦 6. Modais precisam “capturar” o foco
> Modal é uma das coisas que mais quebra acessibilidade

✔ Regras:
  - Ao abrir um modal, o foco vai automaticamente para dentro dele
  - o usuário não pode tabular para fora do modal
  - ao fechar o modal, o foco volta para o elemento que abriu o modal.

❌ Erros comuns:
  - Modal abre e o foco fica “atrás” dele
  - usuário consegue tabular fora do modal
  - foco vai para o topo da página ao fechar
  - ícone de fechar não é focável

### 🟦 7. Componentes interativos precisam ser elementos nativos

> Botões devem ser <button>, links devem ser <a>.

❌ Erro comum:
  - desenvolvedor cria botão usando <div> ou <span>
    - isso quebra:
        - leitor de tela
        - teclabilidade
        - aria roles
        - eventos nativos

##### Como QA testa:
  - Inspecionar: se for ação, tem que ser <button>
      - tente acionar com Enter e Space
  - O leitor de tela deve dizer: “botão”

--------------
🟦 8. Aria Roles
> serve explicar o propósito do elemento, descrever quando a semântica nativa não é suficiente.

Exemplos:
  - role="button"
  - role="dialog"
  - aria-label="Fechar modal"
  - aria-expanded="true/false"
  - aria-live="assertive" (para mensagens dinâmicas)

#### O QA deve verificar:
  - se o leitor de tela anuncia corretamente o componente
  - se avisos dinâmicos são lidos (sucesso/erro em formulários)
  - se elementos complexos têm labels adequados

--------------
## erros estruturais mais comuns 
  - todo site feito com `<div>`, sem headings e landmarks
  - foco invisível ou sem contraste
  - modal que não captura o foco
  - formulários sem labels conectados
  - ordem de foco fora de lógica
  - skip links faltando (“Pular para o conteúdo principal”)
  - elementos clicáveis sem semântica
  - tabela construída sem `<table>`, `<thead>`, `<tr>`, `<th>`


  
