## Interface base para os testes 

<img src="https://github.com/jlateles/estudos-qa/blob/main/arquivos-imagens/interface-vis%C3%A3o-geral.png">
-----

Testes de contraste verificam se texto, ícones e elementos importantes têm contraste suficiente com o plano de fundo para que pessoas com baixa visão, daltonismo ou luminosidade ruim consigam enxergar o conteúdo
> eles seguem padrões definidos pela WCAG 2.2

### 🎯 Por que contraste é importante para o QA?
> Porque contraste insuficiente é um dos erros mais comuns em interfaces e um dos que mais prejudicam
  - Usuários com daltonismo
  - Pessoas com baixa visão
  - Leitura em telas com brilho forte (ex.: celular na rua)
  - Interfaces em tema escuro

Como QA, é importante garantir que nenhuma informação essencial fique ilegível aos usuários, em qualquer contexto de necessidade.

### 📏 Regras oficiais de contraste (WCAG)
Para nível AA (o mais usado pelas empresas):
  - Texto normal: 4.5:1
  - Texto grande (acima de 18px normal ou 14px bold): 3:1
  - Elementos gráficos essenciais (ícones, bordas, estados de foco): 3:1

Para nível AAA (mais exigente):
  - Texto normal: 7:1
  - Texto grande: 4.5:1

### 🧪 O que testar como QA?

##### 1️⃣ Contraste entre texto e fundo
Verifique:
  - Títulos
  - Parágrafos
  - Textos de botão
  - Placeholders
  - Labels
  - Links
  - Mensagens de erro

Erros comuns:
  - Cinza claro no branco
  - Placeholders quase ilegíveis
  - Texto branco em fundo amarelo ou azul claro
  - Verde claro no tema escuro

##### 2️⃣ Contraste de botões e estados
Garanta que o usuário identifique:
  - Botão habilitado vs desabilitado
  - Hover
  - Foco (outline)
  - Botão principal vs secundário

Exemplo de problema comum:
  - Botão “Continuar” desabilitado com cinza #CCCCCC em fundo #FFFFFF
  > contraste baixo, pessoa com baixa visão não vê diferença

##### 3️⃣ Contraste de ícones e elementos essenciais
Inclui:
  - Ícones de alerta
  - Ícones de carrinho
  - Ícones de menu
  - Bordas de campos
  - Indicadores de erro e sucesso

Exemplo de problema comum:
  - O ícone de alerta vermelho em fundo branco ser muito claro
    > perigo de usuário não perceber o erro

##### 4️⃣ Modo claro e modo escuro
Testar ambos é obrigatório!

Erros frequentes:
  - Texto branco em fundo cinza claro no dark mode
  - Botões ficam apagados no modo claro
  - Bordas desaparecem no dark mode
> Muitas empresas passam no teste de contraste no modo claro e esquecem completamente do modo escuro

------

### 🔍 Exemplo prático: 

**Exemplo 1** — **Texto em botão**

Botão:
Fundo #1E88E5
Texto #FFFFFF

Contrast ratio: 4.52:1
→ Teste passa (texto normal nível AA)

Se fosse mais claro, tipo #90CAF9 (azul claro), relação cairia para 2:1 → teste reprova

**Exemplo 2** — **Icone de alerta**

Ícone amarelo #FFEB3B em fundo branco → contraste péssimo.
→ teste reprova
Ícone precisa ser mais escuro ou ter outline.

**Exemplo 3** — **Erro em vermelho**

Erro: texto #E53935
Fundo branco
→ 4.2:1
→ Bom

Mas se usarem um vermelho claro (#EF9A9A), o contraste cai → teste reprova

------------- 
### 🛠️ Ferramentas para testar contraste (como QA)

Extensões e sites:
 - `WebAIM Contrast Checker`
 - `Chrome DevTools → Accessibility → Contrast`
 - `Stark (Figma/Chrome)`
 - `WCAG Contrast Checker (Firefox)`
 - `Color Contrast Analyzer (TPG)`

No navegador:
- `Chrome → F12 → aba Accessibility`
> Mostra contraste e se passa/falha WCAG


### 👀Checklist rápido ✔✔

Antes de aprovar um layout/UI:
  - Texto corpo ≥ 4.5:1
  - Título grande ≥ 3:1
  - Texto de botão legível em todos os estados
  -  Placeholders com contraste suficiente
  -  Labels legíveis SEM depender apenas de cor
  -  Bordas de inputs visíveis
  -  Mensagens de erro claras
  -  Ícones com contraste mínimo de 3:1
  -  Tema claro e tema escuro testados separadamente
  -  Foco visível (outline) com bom contraste
  -  Estados disabled ainda distinguíveis sem depender só da cor
