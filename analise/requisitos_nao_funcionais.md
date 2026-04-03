# Requisitos Não Funcionais — Plataforma U-Bike

**Projeto:** U-Bike IPBeja  
**UC:** Engenharia de Software 2025/2026  
**Fase:** Análise  

---

## Tabela Resumo

| ID      | Categoria         | Descrição resumida                              | Prioridade |
|---------|-------------------|-------------------------------------------------|------------|
| RNF-01  | Desempenho        | Tempo de resposta inferior a 3 segundos         | Alta       |
| RNF-02  | Desempenho        | Suporte a 200 utilizadores simultâneos          | Alta       |
| RNF-03  | Segurança         | Autenticação com credenciais institucionais     | Alta       |
| RNF-04  | Segurança         | Armazenamento encriptado, conformidade RGPD     | Alta       |
| RNF-05  | Segurança         | Controlo de acessos por perfil                  | Alta       |
| RNF-06  | Usabilidade       | Interface responsiva (mobile e desktop)         | Alta       |
| RNF-07  | Usabilidade       | Acessibilidade WCAG 2.1 nível AA               | Média      |
| RNF-08  | Usabilidade       | Facilidade de aprendizagem sem formação prévia  | Média      |
| RNF-09  | Disponibilidade   | Disponibilidade de 99% em período letivo        | Alta       |
| RNF-10  | Fiabilidade       | Recuperação de falhas em menos de 5 minutos     | Alta       |
| RNF-11  | Manutenibilidade  | Arquitetura modular                             | Média      |
| RNF-12  | Manutenibilidade  | Código documentado                              | Média      |
| RNF-13  | Portabilidade     | Compatibilidade com os principais browsers      | Alta       |
| RNF-14  | Conformidade Legal| Cumprimento do RGPD                             | Alta       |

---

## Descrição Detalhada

### Desempenho

#### RNF-01 — Tempo de resposta
- **Descrição:** O sistema deve responder a qualquer pedido do utilizador em menos de 3 segundos em condições normais de rede.
- **Prioridade:** Alta
- **Verificação:** Testes de carga com ferramentas como Apache JMeter, medindo o tempo de resposta médio e o percentil 95.

#### RNF-02 — Capacidade concorrente
- **Descrição:** O sistema deve suportar pelo menos 200 utilizadores simultâneos sem degradação de desempenho perceptível.
- **Prioridade:** Alta
- **Verificação:** Testes de stress com simulação de 200 sessões concorrentes, verificando que o tempo de resposta se mantém abaixo do limite definido em RNF-01.

---

### Segurança

#### RNF-03 — Autenticação
- **Descrição:** O acesso ao sistema deve ser feito através de autenticação com credenciais institucionais (email do IPBeja), com suporte a recuperação de password segura.
- **Prioridade:** Alta
- **Verificação:** Testes funcionais de login com credenciais válidas e inválidas; validação do fluxo de recuperação de password.

#### RNF-04 — Proteção de dados pessoais
- **Descrição:** Os dados pessoais dos utilizadores devem ser armazenados de forma encriptada (mínimo AES-256), em conformidade com o RGPD.
- **Prioridade:** Alta
- **Verificação:** Auditoria à base de dados confirmando encriptação em repouso; revisão da política de privacidade.

#### RNF-05 — Controlo de acessos
- **Descrição:** Devem existir perfis de utilizador distintos (estudante, administrador) com permissões diferenciadas. Um estudante não pode aceder a funcionalidades de gestão.
- **Prioridade:** Alta
- **Verificação:** Testes de controlo de acesso tentando executar operações de administrador com conta de estudante.

---

### Usabilidade

#### RNF-06 — Interface responsiva
- **Descrição:** A plataforma deve ser acessível em dispositivos móveis (iOS e Android) e desktop, adaptando-se automaticamente ao tamanho do ecrã.
- **Prioridade:** Alta
- **Verificação:** Testes de renderização nos principais dispositivos e resoluções (320px a 1920px de largura).

#### RNF-07 — Acessibilidade
- **Descrição:** A interface deve seguir as diretrizes WCAG 2.1 (nível AA), garantindo acessibilidade a utilizadores com necessidades especiais (contraste, navegação por teclado, compatibilidade com leitores de ecrã).
- **Prioridade:** Média
- **Verificação:** Validação automática com ferramentas como Axe ou Lighthouse; revisão manual dos critérios WCAG 2.1 AA.

#### RNF-08 — Facilidade de aprendizagem
- **Descrição:** Um utilizador novo deve conseguir realizar as operações básicas (reservar, devolver, consultar histórico) sem necessidade de formação prévia, em menos de 10 minutos de exploração.
- **Prioridade:** Média
- **Verificação:** Testes de usabilidade com utilizadores reais (estudantes), medindo o tempo necessário para completar tarefas básicas sem assistência.

---

### Disponibilidade e Fiabilidade

#### RNF-09 — Disponibilidade
- **Descrição:** O sistema deve estar disponível 99% do tempo durante o período letivo, excluindo períodos de manutenção previamente comunicados.
- **Prioridade:** Alta
- **Verificação:** Monitorização contínua com ferramentas de uptime monitoring; cálculo mensal da taxa de disponibilidade.

#### RNF-10 — Recuperação de falhas
- **Descrição:** Em caso de falha inesperada, o sistema deve recuperar automaticamente e sem perda de dados em menos de 5 minutos.
- **Prioridade:** Alta
- **Verificação:** Testes de recuperação simulando falhas de servidor e verificando a integridade dos dados após recuperação.

---

### Manutenibilidade

#### RNF-11 — Modularidade
- **Descrição:** O sistema deve ser desenvolvido de forma modular, permitindo adicionar novas funcionalidades (ex: novos indicadores de saúde) sem alterar o núcleo existente.
- **Prioridade:** Média
- **Verificação:** Revisão da arquitetura do código confirmando separação clara de responsabilidades (ex: padrão MVC ou equivalente).

#### RNF-12 — Documentação do código
- **Descrição:** O código deve estar documentado de forma a que um novo programador consiga compreender e modificar qualquer módulo sem necessidade de apoio externo.
- **Prioridade:** Média
- **Verificação:** Revisão do código confirmando a presença de comentários/docstrings nos módulos principais.

---

### Portabilidade

#### RNF-13 — Compatibilidade de browsers
- **Descrição:** A plataforma web deve funcionar corretamente nos browsers mais utilizados: Chrome, Firefox, Safari e Edge (versões lançadas nos últimos 2 anos).
- **Prioridade:** Alta
- **Verificação:** Testes funcionais nos quatro browsers indicados, validando as principais funcionalidades.

---

### Conformidade Legal

#### RNF-14 — Cumprimento do RGPD
- **Descrição:** O sistema deve permitir ao utilizador consultar, exportar e solicitar a eliminação dos seus dados pessoais, em cumprimento do Regulamento Geral de Proteção de Dados (RGPD - Regulamento UE 2016/679).
- **Prioridade:** Alta
- **Verificação:** Validação funcional das opções de consulta, exportação e eliminação de dados; confirmação que nenhum dado é partilhado com terceiros sem consentimento explícito.

---

## Referências


- WCAG 2.1: https://www.w3.org/TR/WCAG21/
- RGPD: https://eur-lex.europa.eu/legal-content/PT/TXT/?uri=CELEX%3A32016R0679
- ISO/IEC 25010 — Modelo de qualidade de software
