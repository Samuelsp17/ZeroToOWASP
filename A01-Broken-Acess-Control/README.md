# 🔐 Broken Access Control (Controle de Acesso Quebrado)

## 📌 O que é?

Broken Access Control ocorre quando uma aplicação **não impõe corretamente as regras de autorização**, permitindo que usuários acessem funcionalidades ou dados que **não deveriam estar disponíveis para eles**.

Essa falha é **a número 1 do OWASP Top 10 (2021)**, por ser extremamente comum e de alto impacto.

---

## 🚨 Exemplos Comuns de Broken Access

| Tipo de Falha                     | Descrição |
|----------------------------------|-----------|
| **IDOR (Insecure Direct Object Reference)** | O sistema permite acesso a objetos (dados, arquivos, etc.) apenas com alteração de identificadores, sem verificar a propriedade. |
| **Elevação de privilégios**       | Um usuário comum consegue realizar ações administrativas (como alterar permissões, excluir usuários, etc.). |
| **Exposição de funções ocultas** | Funcionalidades não visíveis no frontend ainda podem ser acessadas diretamente por URL ou requisição. |
| **Forçar navegação (forced browsing)** | Acesso a rotas ou arquivos diretamente, mesmo sem links visíveis. |
| **Falhas em regras baseadas em roles** | A aplicação permite ações além do permitido para um determinado papel (role). |

---

## 🕵️‍♂️ Como identificar

- Testar URLs modificadas manualmente (`/admin`, `/delete?id=2`, `/user/3`).
- Observar se a aplicação retorna dados de outros usuários com alteração de parâmetros.
- Tentar repetir ações de um usuário com menos privilégio e ver se o sistema bloqueia corretamente.
- Inspecionar o frontend para funções escondidas (botões, links, campos) que ainda podem ser chamadas diretamente.

---

## ⚠️ Impactos

- Vazamento de dados sensíveis.
- Acesso ou modificação de informações de outros usuários.
- Controle administrativo por usuários não autorizados.
- Comprometimento completo da aplicação ou do sistema.

---

## 🛡️ Como mitigar

| Prática                          | Ação Recomendável |
|----------------------------------|-------------------|
| **Verificações de acesso no servidor** | Nunca confie em validações feitas apenas no frontend. Sempre valide permissões no back-end. |
| **Controle de acesso baseado em contexto de sessão** | Use os dados do usuário logado (sessão/token) para validar ações, e não valores fornecidos pelo usuário. |
| **Minimizar exposição de rotas** | APIs e URLs sensíveis devem estar protegidas por autenticação e autorização adequadas. |
| **Logs e monitoramento de acessos** | Detectar padrões de abuso ou tentativa de escalonamento de privilégio. |
| **Revisões regulares de permissões** | Garanta que perfis, roles e recursos estão corretamente mapeados. |

---

## ✅ Resumo

- Broken Access Control é uma das **falhas mais perigosas e recorrentes** em aplicações modernas.
- **Validação de permissões deve sempre ocorrer no lado do servidor**, e ser aplicada a **todas as rotas e ações**.
- Testes contínuos, revisões e uso de boas práticas de segurança reduzem drasticamente esse tipo de vulnerabilidade.

---

## 📚 Referência

- [OWASP Top 10: A01 - Broken Access Control (2021)](https://owasp.org/Top10/A01_2021-Broken_Access_Control/)