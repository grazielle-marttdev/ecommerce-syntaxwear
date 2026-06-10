# Planejamento Técnico: SyntaxWear 2.0 (React + TypeScript)

Este documento detalha a estratégia de upgrade do site estático SyntaxWear para uma aplicação Single Page Application (SPA) moderna, focada em performance, escalabilidade e experiência do usuário.

## 1. Arquitetura de Rotas (Navegação Dinâmica)

Utilizaremos o `react-router-dom` para gerenciar a navegação sem recarregar a página.

### Mapa de URLs:
- **` / ` (Home):** Landing page com Hero Section e Grid de destaques.
- **`/produtos/:categoria`:** Página dinâmica que filtra produtos.
    - Ex: `/produtos/casual`, `/produtos/esporte`, `/produtos/masculino`.
- **`/produto/:id`:** Página de detalhes de um item específico.
- **`/carrinho`:** Resumo dos itens selecionados e simulação de checkout.
- **`/sobre`:** Informações sobre a marca.

## 2. Gerenciamento de Estado (O "Cérebro")

Para que o site "ganhe vida" e os componentes conversem entre si, utilizaremos:

- **Context API (`CartContext`):**
    - Armazenará a lista de produtos no carrinho.
    - Função `addToCart`, `removeFromCart` e `updateQuantity`.
    - Cálculo automático do total e da quantidade de itens para exibir no ícone da sacola no Header.
- **LocalStorage:**
    - Persistência dos dados para que o carrinho não esvazie ao atualizar a página.

## 3. Estratégia de Dados (API de Tênis)

Como as APIs públicas gratuitas (como FakeStoreAPI) não possuem foco em calçados, adotaremos a estratégia de **Mock API**:
- Criaremos um arquivo `src/data/products.json` com dados estruturados (ID, nome, preço, categoria, descrição e URL da imagem).
- Criaremos um **Service** no React que utiliza `fetch` ou uma `Promise` simulada para buscar esses dados, preparando o projeto para uma futura integração com um backend real.

## 4. Componentização

O código será quebrado em partes menores e reutilizáveis:

- **Core Components:** `Header`, `Footer`, `Button`, `Layout`.
- **Product Components:** `ProductCard`, `ProductGrid`, `CategorySlider`.
- **Interactive Components:** `CartDrawer` (menu lateral do carrinho), `SearchModal`.

## 5. Estrutura de Pastas Sugerida

```text
src/
├── assets/             # Imagens, ícones e fontes
├── components/         # Componentes reutilizáveis (UI)
│   ├── Header/
│   ├── Footer/
│   └── ProductCard/
├── context/            # Estados globais (Context API)
├── data/               # Mock de dados (JSON)
├── hooks/              # Hooks personalizados
├── pages/              # Páginas da aplicação (Routes)
│   ├── Home/
│   ├── ProductDetails/
│   └── ProductListing/
├── services/           # Chamadas de "API"
├── styles/             # CSS Global e Variáveis
└── types/              # Definições de tipos TypeScript
```

## 6. Próximos Passos (Roadmap)

1. **Setup:** Inicializar projeto com Vite + TypeScript.
2. **Global Styles:** Migrar `variables.css`, `reset.css` e `base.css`.
3. **Layout Base:** Criar os componentes de `Header` e `Footer`.
4. **Routing:** Configurar as primeiras rotas (Home e Sobre).
5. **Data Flow:** Criar o Mock de produtos e o serviço de busca.
6. **Cart Logic:** Implementar o `CartContext` e a funcionalidade de adicionar itens.
7. **Refinamento:** Adicionar animações de transição e estados de loading.
