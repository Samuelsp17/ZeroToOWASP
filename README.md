# Bug Bounty — OWASP Top 10 (2021)

![Banner OWASP](https://owasp.org/assets/images/logo.png)

> Aviso Legal  
> Este repositório é exclusivamente para fins educacionais. Jamais aplique qualquer conhecimento aqui descrito em sistemas que você não possui ou não tem autorização explícita para testar. Isso é considerado crime em praticamente todas as jurisdições.  
> Conhecimento não é crime, mas a forma como você o usa, pode ser. Use com sabedoria.

---

## Objetivo

Este repositório explora as principais vulnerabilidades em aplicações web segundo a [OWASP Top 10 - 2021](https://owasp.org/Top10/). O foco está na identificação, exploração e entendimento dessas falhas, usando técnicas manuais e ferramentas desenvolvidas principalmente em Python e JavaScript.

---

## OWASP Top 10 - 2021

Aqui estão as 10 vulnerabilidades mais críticas em aplicações web, conforme definidas pela OWASP:

---

### [1. A01:2021 — Broken Access Control (Controle de Acesso Quebrado)](https://github.com/Samuelsp17/ZeroToOWASP/tree/main/A01-Broken-Acess-Control)  
Permite que usuários não autorizados acessem funcionalidades ou dados restritos.  
Exemplos:
- Acesso a APIs privadas
- Modificação de URLs para visualizar dados de outros usuários

---

### [2. A02:2021 — Cryptographic Failures (Falhas Criptográficas)](https://github.com/Samuelsp17/ZeroToOWASP/tree/main/A02-Cryptographic-Failures)  
Proteção inadequada de dados sensíveis como senhas, informações pessoais e chaves.  
Exemplos:
- Dados transmitidos sem criptografia
- Uso de algoritmos criptográficos fracos
- Certificados SSL expirados

---

### [3. A03:2021 — Injection (Injeção de Código)](https://github.com/Samuelsp17/ZeroToOWASP/tree/main/A03-Injection)  
Inserção de comandos maliciosos em entradas mal validadas.  
Tipos comuns:
- SQL Injection  
- Command Injection  
- LDAP Injection

---

### [4. A04:2021 — Insecure Design (Design Inseguro)](https://github.com/Samuelsp17/ZeroToOWASP/tree/main/A04-Insecure-Design)  
Ausência de boas práticas de segurança na arquitetura da aplicação.  
Exemplos:
- Falta de validação de limites
- Regras de negócio mal definidas

---

### [5. A05:2021 — Security Misconfiguration (Configuração de Segurança Incorreta)](https://github.com/Samuelsp17/ZeroToOWASP/tree/main/A05-Security-Misconfiguration)
Configurações mal feitas que expõem a aplicação a riscos.  
Exemplos:
- Diretórios expostos
- Debug ativado em produção
- Permissões excessivas

---

### [6. A06:2021 — Vulnerable and Outdated Components (Componentes Vulneráveis e Desatualizados)](https://github.com/Samuelsp17/ZeroToOWASP/tree/main/A06-Vulnerable-and-Outdated-Componets)  
Uso de bibliotecas ou frameworks com falhas conhecidas.  
Exemplo:
- Dependências JavaScript desatualizadas e não corrigidas

---

### [7. A07:2021 — Identification and Authentication Failures (Falhas de Identificação e Autenticação)](https://github.com/Samuelsp17/ZeroToOWASP/tree/main/A07-Indentification-and-Authentication-Failures)  
Erros em login, gerenciamento de sessões e autenticação.  
Exemplos:
- Ataques de força bruta
- Tokens previsíveis ou reutilizáveis

---

### [8. A08:2021 — Software and Data Integrity Failures (Falhas na Integridade de Software e Dados)](https://github.com/Samuelsp17/ZeroToOWASP/tree/main/A08-Software-and-Data-Integrity-Failures)  
Atualizações ou bibliotecas sem verificação de integridade.  
Exemplos:
- Falta de assinatura digital em pacotes
- Supply chain attacks

---

### [9. A09:2021 — Security Logging and Monitoring Failures (Falhas de Registro e Monitoramento de Segurança)](https://github.com/Samuelsp17/ZeroToOWASP/tree/main/A09-Security-Logging-and-Monitoring-Failures)  
Sem registros adequados, a detecção de incidentes se torna difícil.  
Exemplos:
- Logs inacessíveis ou inexistentes
- Falta de alertas automáticos

---

### [10. A10:2021 — Server-Side Request Forgery (SSRF) (Forjamento de Requisição no Lado do Servidor)](https://github.com/Samuelsp17/ZeroToOWASP/tree/main/A10-SSRF)  
Engana o servidor para realizar requisições maliciosas para redes internas ou serviços externos.  
Exemplo:**
- Acesso indevido a serviços internos via requisições manipuladas

---

## Contribuições

Este projeto está aberto a melhorias, sugestões e colaborações. Pull requests são bem-vindos.

---

## Licença

[MIT License](LICENSE)
