# Proposta Técnica: SyntaxWear 2.0 - E-commerce de Próxima Geração

## 1. Visão Geral
Este documento detalha o plano de evolução do projeto **SyntaxWear**, transformando um site estático (HTML/CSS) em uma aplicação Single Page Application (SPA) moderna utilizando **React**, **TypeScript** e consumo de **API Simulada (Mock API)**.

O objetivo é criar uma ferramenta de estudo prático para revisão de conceitos fundamentais e avançados de desenvolvimento Front-end, mantendo a identidade visual e temática de sneakers.

## 2. Tecnologias Propostas
- **Core:** React (Vite)
- **Linguagem:** TypeScript (para garantir segurança e tipagem de dados)
- **Estilização:** CSS Modules ou Vanilla CSS (aproveitando o trabalho já feito)
- **Gerenciamento de Estado:** Context API (para o Carrinho de Compras)
- **Consumo de Dados:** Fetch API com **Mock API (JSON Local)** para garantir uma temática consistente de tênis.
- **Roteamento:** React Router DOM (para navegação entre categorias e detalhes).

## 3. Funcionalidades de "Vida Real"
1.  **Catálogo Dinâmico e Temático:** Os produtos serão buscados de uma Mock API customizada, permitindo exibir modelos reais de tênis (como o Krypton One), com preços, descrições e fotos de alta qualidade.
2.  **Sistema de Carrinho:**
    - Adicionar/Remover itens.
    - Alterar quantidade.
    - Cálculo de subtotal e total em tempo real.
    - Persistência no `localStorage`.
3.  **Filtros e Categorias Dinâmicas:** Navegação funcional entre as categorias (Casual, Esporte, Moderno, Futurista) e gêneros (Masculino, Feminino) através de parâmetros na URL.
4.  **Página de Detalhes:** Ao clicar em um produto, abrir uma página exclusiva com detalhes técnicos buscados pelo ID.
5.  **Simulação de Checkout:** Uma tela de resumo do pedido antes da "finalização".

## 4. Divisão Sugerida (caso seja colaborativo)

Para um estudo colaborativo, as tarefas podem ser divididas em dois eixos:

### **Pilar A: Infraestrutura e Dados**
- Configuração inicial do Vite + TS.
- Criação do Mock Data (JSON) e dos Services de busca.
- Implementação da Context API para o Carrinho.
- Lógica de persistência (LocalStorage).

### **Pilar B: Componentização e Interface**
- Transformar as seções atuais (Hero, Category, Grid) em Componentes React.
- Mapeamento dinâmico dos dados para os cards de produto.
- Gerenciamento de rotas (Home vs. Listagem por Categoria vs. Detalhes).
- Feedback visual (Loading states e Skeleton screens).

## 5. Próximos Passos
1.  Criar a estrutura base do projeto com Vite.
2.  Mapear os estilos CSS atuais para o novo formato de componentes.
3.  Implementar o Mock de produtos e o primeiro `fetch` para listar os itens na Home.

---
*Este projeto visa solidificar conhecimentos de fluxo de dados, ciclo de vida de componentes e manipulação de estado global.*
