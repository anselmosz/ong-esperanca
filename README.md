# ONG Esperança

## Descrição

Este projeto é uma plataforma institucional estática para uma ONG fictícia, com foco em apresentação de projetos sociais, formação de voluntariado, campanhas de doação e relacionamento com a comunidade. O objetivo principal foi aplicar CSS3 puro com organização modular, layout responsivo e acessibilidade básica de acordo com as diretrizes da entrega.

## Como abrir

Basta abrir o arquivo `index.html` no navegador. Não é necessário servidor web nem backend.

## Estrutura de pastas

```text
/ (raiz do projeto)
├── index.html
├── projetos.html
├── cadastro.html
├── README.md
├── assets/
    ├── favicon.ico
│   ├── icons/
│   │   └── logo.svg
│   └── images/
│       ├── hero.svg
│       ├── about.svg
│       ├── project-education.svg
│       ├── project-health.svg
│       ├── project-environment.svg
│       ├── project-culture.svg
│       ├── project-food.svg
│       ├── project-community.svg
│       ├── gallery-1.svg
│       ├── gallery-2.svg
│       ├── gallery-3.svg
│       ├── gallery-4.svg
│       ├── gallery-5.svg
│       └── gallery-6.svg
└── css/
    ├── main.css
    ├── base/
    │   ├── variables.css
    │   ├── reset.css
    │   └── typography.css
    ├── layout/
    │   ├── container.css
    │   ├── grid-12.css
    │   ├── header.css
    │   └── footer.css
    ├── components/
    │   ├── navigation.css
    │   ├── buttons.css
    │   ├── cards.css
    │   ├── forms.css
    │   ├── feedback.css
    │   └── badges.css
    └── pages/
        ├── home.css
        ├── projetos.css
        └── cadastro.css
```

- `assets/icons`: elementos de marca e identidade visual.
- `assets/images`: ilustrações e fotos estilizadas em SVG, locais e com licença de uso livre para demonstração.
- `css/base`: define variáveis de design, reset e tipografia.
- `css/layout`: estrutura da página, grid e cabeçalho/rodapé.
- `css/components`: botões, cards, formulários, feedback e badges.
- `css/pages`: estilos específicos de cada página.

## Sistema de design

### Cores principais

| Nome | Valor |
|---|---|
| Verde principal | `#0e7c66` |
| Verde escuro | `#0b5d4b` |
| Laranja destaque | `#c2410c` |
| Fundo neutro | `#f9fafb` |
| Texto principal | `#111827` |
| Texto secundário | `#374151` |
| Sucesso | `#15803d` |
| Aviso | `#b45309` |
| Erro | `#b91c1c` |
| Informação | `#0369a1` |

### Tipografia

| Nome | Valor |
|---|---|
| `--font-size-xs` | `0.75rem` |
| `--font-size-sm` | `0.875rem` |
| `--font-size-md` | `1rem` |
| `--font-size-lg` | `1.25rem` |
| `--font-size-xl` | `1.5rem` |
| `--font-size-2xl` | `2rem` |
| `--font-size-3xl` | `2.5rem` |

### Espaçamento

| Nome | Valor |
|---|---|
| `--space-1` | `0.5rem` (8px) |
| `--space-2` | `1rem` (16px) |
| `--space-3` | `1.5rem` (24px) |
| `--space-4` | `2rem` (32px) |
| `--space-6` | `3rem` (48px) |
| `--space-8` | `4rem` (64px) |

### Breakpoints

| Nome | Largura mínima |
|---|---|
| `sm` | `480px` |
| `md` | `768px` |
| `lg` | `1024px` |
| `xl` | `1280px` |
| `2xl` | `1536px` |

## Componentes

- `.btn` — botão base; variações `.btn--primary`, `.btn--secondary`, `.btn--outline`, `.btn--disabled`.
- `.card` — card de projeto; elementos `.card__image`, `.card__body`, `.card__footer`.
- `.badge` — etiqueta de categoria; variações `.badge--education`, `.badge--health`, `.badge--environment`, `.badge--culture`.
- `.tag` — rótulo visual para destaque.
- `.form-card`, `.form-field`, `.form-group` — formulário acessível com validação visual.
- `.alert` — alertas com variações por status.
- `.toast` — mensagem flutuante aberta via `:target`.
- `.modal` — modal simples usando `:target` e CSS puro.

## Decisões técnicas

- O layout geral usa Grid para organizar a estrutura da página, as áreas de conteúdo e o sistema de colunas.
- Flexbox foi usado para navegação, alinhamento de itens internos, botões e blocos de componentes.
- O menu responsivo utiliza checkbox escondido com `:checked` em CSS, permitindo abrir e fechar o menu sem JavaScript.
- O submenu de projetos aparece em telas maiores por `:hover` e `:focus-within`.
- O modal e o toast funcionam com o seletor `:target`, que responde ao fragmento da URL. Isso permite abrir o conteúdo sem JavaScript, com a limitação de que não há fechamento via tecla `Esc` nem foco preso dentro do modal.

## Limitações conhecidas

- Toast e modal são implementados apenas com CSS; portanto, não há fechamento por tecla `Esc` nem foco automático.
- Não existe máscara JavaScript de CPF, telefone ou CEP; os formatos esperados aparecem em placeholders e mensagens de ajuda.
- O menu depende do checkbox como estado; por isso, o comportamento é simples, estático e sem animações avançadas.

## Créditos de imagens

As ilustrações utilizadas neste projeto foram criadas localmente em SVG dentro do repositório para manter o projeto autônomo, sem dependência de bibliotecas externas.

## Observação final

A entrega prioriza legibilidade, simplicidade e organização do código, seguindo a proposta da Entrega II: CSS3 escrito à mão, modularizado e responsivo, sem JavaScript e sem frameworks.
