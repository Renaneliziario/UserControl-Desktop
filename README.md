# UserControl-Desktop

![Java](https://img.shields.io/badge/Java-SE%208+-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Swing](https://img.shields.io/badge/GUI-Java%20Swing-4A90D9?style=flat)
![Pattern](https://img.shields.io/badge/Pattern-MVC%20%7C%20DAO-6DB33F?style=flat)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen?style=flat)

> Aplicação desktop de gerenciamento de clientes (CRUD completo) construída com Java Swing, demonstrando domínio de **Orientação a Objetos**, **padrão DAO** com múltiplas implementações intercambiáveis e **inversão de dependência** na prática.

---

## ✨ Destaques Técnicos

- **Duas implementações do padrão DAO** (`HashMap` e `HashSet`) trocáveis sem alterar uma linha da lógica de negócio — demonstração prática de polimorfismo e Interface Segregation
- **Inversão de dependência:** a camada de apresentação conhece apenas `IClienteDAO`, nunca a implementação concreta
- **`equals` / `hashCode` corretos** na entidade `Cliente`, garantindo comportamento previsível em coleções Java
- **Separação MVC** clara entre camada de apresentação (Swing), serviço e domínio

---

## 🏗️ Arquitetura

```
Apresentação (Swing / JOptionPane)
        │
        ▼
IClienteDAO  ◄──────────────────────────┐
        │                               │
  ClienteMapDAO               ClienteSetDAO
  (HashMap)                   (HashSet)
```

A interface `IClienteDAO` permite substituir a implementação em uma linha — o mesmo contrato que conectaria este projeto a um banco de dados real (como nos projetos seguintes).

---

## 🛠️ Tecnologias

| Tecnologia | Uso |
|:---|:---|
| Java SE 8+ | Linguagem principal |
| Java Swing / JOptionPane | Interface gráfica desktop |
| HashMap / HashSet | Implementações de persistência em memória |

---

## 🚀 Como Executar

**Pré-requisitos:** JDK 8+ e uma IDE (Eclipse ou IntelliJ)

```bash
# 1. Importe o projeto na sua IDE como "Java Project"
# 2. Certifique-se que a pasta src/ está no Build Path
# 3. Execute a classe principal:
br.com.renaneliziario.Cadastro
```

---

## 📌 Contexto no Portfólio

Este é o **projeto 1 de 5** de uma trilha de evolução técnica intencional:

`UserControl (POO)` → `QualityGuard (Testes)` → `SalesSystem-JDBC` → `SalesPersistence-JPA` → `Sales-Microservices`

---

*Desenvolvido por [Renan Queiroz Eliziario](https://www.linkedin.com/in/renaneliziario/) · [Portfólio completo no GitHub](https://github.com/Renaneliziario)*
