# Proposta Técnica: SyntaxWear 2.0 - E-commerce de Próxima Geração

## 1. Visão Geral
Este documento detalha o plano de evolução do projeto **SyntaxWear**, transformando um site estático (HTML/CSS) em uma aplicação Single Page Application (SPA) moderna utilizando **React**, **TypeScript** e consumo de **API Real**.

O objetivo é criar uma ferramenta de estudo prático para revisão de conceitos fundamentais e avançados de desenvolvimento Front-end.

## 2. Tecnologias Propostas
- **Core:** React (Vite)
- **Linguagem:** TypeScript (para garantir segurança e tipagem de dados da API)
- **Estilização:** CSS Modules ou Vanilla CSS (aproveitando o trabalho já feito)
- **Gerenciamento de Estado:** Context API (para o Carrinho de Compras)
- **Consumo de Dados:** Fetch API ou Axios com [FakeStoreAPI](https://fakestoreapi.com/)
- **Roteamento:** React Router DOM

## 3. Funcionalidades de "Vida Real"
1.  **Catálogo Dinâmico:** Os produtos não estarão mais no HTML. Eles serão buscados na FakeStoreAPI, permitindo ver preços, descrições e imagens reais.
2.  **Sistema de Carrinho:**
    - Adicionar/Remover itens.
    - Alterar quantidade.
    - Cálculo de subtotal e total em tempo real.
    - Persistência no `localStorage`.
3.  **Filtros e Categorias:** Navegação funcional entre Masculino, Feminino e Eletrônicos (ou mapear para as categorias da API).
4.  **Página de Detalhes:** Ao clicar em um tênis/produto, abrir uma página exclusiva com detalhes técnicos.
5.  **Simulação de Checkout:** Uma tela de resumo do pedido antes da "finalização".

## 4. Divisão Sugerida (caso seja colaborativo)

Para um estudo colaborativo, as tarefas podem ser divididas em dois eixos:

### **Pilar A: Infraestrutura e Dados**
- Configuração inicial do Vite + TS.
- Criação dos Services (funções que buscam dados na API).
- Implementação da Context API para o Carrinho.
- Lógica de persistência (LocalStorage).

### **Pilar B: Componentização e Interface**
- Transformar as seções atuais (Hero, Category, Grid) em Componentes React.
- Mapeamento (map) dos dados da API para os cards de produto.
- Gerenciamento de rotas (Home vs. Carrinho vs. Detalhes).
- Feedback visual (Loading states e Skeleton screens).

## 5. Próximos Passos
1.  Criar o repositório base com Vite.
2.  Mapear os estilos CSS atuais para o novo formato de componentes.
3.  Implementar o primeiro `fetch` para listar os produtos na Home.

---
*Este projeto visa solidificar conhecimentos de fluxo de dados, ciclo de vida de componentes e manipulação de estado global.*