
### Gestão de Estoque

### Descrição

Este projeto foi desenvolvido como parte do curso de **Análise e Desenvolvimento de Sistemas (ADS)**, durante a **quarta fase** da faculdade. O objetivo principal é criar uma solução de gestão de estoque eficiente, permitindo o controle e monitoramento de produtos através de seu respectivo projeto.

## Funcionalidades

- **Gerenciamento de Usuários (Funcionários):** Registrar, visualizar, deletar e editar todos os funcionários da empresa, permitindo a gestão de suas funções em cada projeto.
- **Projetos:** Criar e gerenciar projetos, vinculando funcionários e produtos, permitindo a organização e execução das tarefas de acordo com a necessidade de cada projeto.
- **Compra:** Registrar e gerenciar compras de produtos, acompanhando o histórico de aquisições e integrando com o estoque automaticamente.
- **Item:** Gerenciar os itens do estoque, com controle preciso de suas características como quantidade, localização e movimentações.
- **Cliente:** Registrar e gerenciar os dados dos clientes, facilitando o controle de pedidos e personalizações de acordo com suas demandas.
- **Fornecedor:** Cadastrar e gerenciar fornecedores, garantindo que todas as transações e aquisições sejam documentadas e rastreáveis.


### Diagrama Entidades do Sistema de Gestão de Estoque

```mermaid
erDiagram
    CUSTOMER {
        string Nome_Completo
        string Cnpj
        string Email
    }

    USER {
        string full_name
        string enrollment
        string email
    }

    PROJECTS {
        string name
        string instituition
        string project_manager
        string tech_responsible
    }

    SALE {
        string Item
        string electronic_invoice
        int quantity
        boolean is_received
    }

    SUPPLIER {
        string corporate_name
        string cnpj
        string phone
        string email
        string address
    }

    ITEM {
        string Nome
        string Armazenamento
        string Descricao
        int Quantidade
    }

    CUSTOMER ||--o{ SALE : "Realiza"
    SALE ||--|{ ITEM : "Contém"
    PROJECTS ||--o{ USER : "Gerencia"
    SALE ||--o{ SUPPLIER : "Adquirido de"
    PROJECTS ||--o{ CUSTOMER : "Desenvolvido para"
```

### Tecnologias Utilizadas

- **Frontend:** TypeScript, Next.js, Node.js, React.
- **Backend:** GoLang, ServiceWeaver, SQLC, Fiber e Boneless.
- **Banco de Dados:** MySQL e AWS S3
- **Outros:** Docker Compose



### Colaboradores

<div style="display: flex; flex-direction: row; align-items: center; width: 100%; gap: 10px; flex-wrap: wrap;">

  <div style="text-align: center;">
    <a href="https://github.com/Ssalvador221">
      <img src="https://github.com/Ssalvador221.png" alt="João Salvador" width="50" height="50">
      <br>João Salvador
    </a>
  </div>

  <div style="text-align: center;">
    <a href="https://github.com/matiasgonzalvez">
      <img src="https://github.com/matiasgonzalvez.png" alt="Matias Gonzalvez" width="50" height="50">
      <br>Matias Gonzalvez
    </a>
  </div>

  <div style="text-align: center;">
    <a href="https://github.com/JFP79">
      <img src="https://github.com/JFP79.png" alt="Jael Felipe" width="50" height="50">
      <br>Jael Felipe
    </a>
  </div>

  <div style="text-align: center;">
    <a href="https://github.com/felipeloche">
      <img src="https://github.com/felipeloche.png" alt="Felipe Loche" width="50" height="50">
      <br>Felipe Loche
    </a>
  </div>

</div>
