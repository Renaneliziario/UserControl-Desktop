# UserControl-Desktop: Gerenciador de Usuários com Java Swing e Arquitetura MVC

Este é o primeiro projeto da trilha de especialização Back-End Java, focado nos fundamentos da **Programação Orientada a Objetos (POO)**, padrões de projeto e interfaces gráficas (GUI). O sistema permite a gestão completa (CRUD) de clientes em um ambiente desktop resiliente.

---

## 🏗️ Arquitetura e Design Patterns

O projeto foi estruturado seguindo princípios de engenharia de software para garantir manutenibilidade e escalabilidade:

1.  **MVC (Model-View-Controller):** Separação clara entre a lógica de apresentação (Swing), as regras de negócio e o modelo de dados.
2.  **DAO (Data Access Object):** Abstração da camada de persistência. O sistema utiliza interfaces (`IClienteDAO`) para permitir a troca fácil entre implementações (ex: Memória, JDBC ou JPA) sem afetar a lógica de negócio.
3.  **Injeção de Dependência:** Uso de polimorfismo para injetar a implementação concreta do DAO, facilitando testes unitários e extensibilidade.

---

## 🛠️ Tecnologias Utilizadas

*   **Java SE (LTS):** Core da linguagem, utilizando coleções avançadas (`HashMap`, `HashSet`).
*   **Java Swing:** Construção de interfaces gráficas baseadas em eventos e diálogos interativos (`JOptionPane`).
*   **Encapsulamento & Tipagem Forte:** Uso de `Long` para CPFs/Telefones e `Integer` para numeração, garantindo integridade dos dados.

---

## 🧩 Modelo de Domínio

A entidade principal `Cliente` reflete um cadastro completo e validado:

| Atributo | Tipo | Descrição |
| :--- | :--- | :--- |
| `nome` | `String` | Nome completo do cliente |
| `cpf` | `Long` | Identificador único (chave primária em memória) |
| `tel` | `Long` | Contato telefônico |
| `end` | `String` | Logradouro |
| `numero` | `Integer` | Número da residência |
| `cidade` | `String` | Cidade de residência |
| `estado` | `String` | Unidade Federativa (UF) |

---

## 📂 Estrutura do Projeto

```text
src/
└── br/com/renan/
    ├── domain/      # Entidades (Model)
    ├── dao/         # Interfaces e Implementações de Persistência (DAO)
    └── App.java     # Classe Principal / Controller / View
```

---

## 🚀 Como Executar

### Pré-requisitos
*   Java JDK 8 ou superior instalado.
*   IDE de sua preferência (Eclipse, IntelliJ ou VS Code).

### Passos
1.  Importe o projeto como um projeto Java existente.
2.  Certifique-se de que a pasta `src` está configurada no seu *Build Path*.
3.  Execute a classe `br.com.renan.App` (ou a classe principal contendo o `main`).
4.  Interaja com o sistema através das janelas de diálogo para cadastrar, consultar ou excluir usuários.

---

## 📌 Evolução Técnica
Este projeto marca o início da jornada, onde foram consolidados os conceitos de **encapsulamento, coleções e tratamento de eventos**. A partir desta base, os projetos seguintes evoluíram para persistência em bancos de dados relacionais (JDBC/JPA) e, finalmente, para arquiteturas de microserviços.

---
*Desenvolvido por Renan Queiroz Eliziario como parte do portfólio profissional.*
