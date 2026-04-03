# Atores do Sistema — Plataforma U-Bike

**Projeto:** U-Bike IPBeja  
**UC:** Engenharia de Software 2025/2026  
**Fase:** Análise — Casos de Uso  

---

## Visão Geral

O sistema U-Bike envolve **5 atores**, divididos em dois tipos:

| Tipo | Ator | Descrição resumida |
|------|------|--------------------|
| Abstrato | Utilizador | Ator genérico — base de Estudante e Administrador |
| Primário | Estudante | Especialização de Utilizador — utilizador principal da plataforma |
| Primário | Administrador | Especialização de Utilizador — gestor da frota e da plataforma |
| Secundário | Sistema GPS / Monitorização | Fornece dados de localização e percurso |
| Secundário | Sistema de Autenticação Institucional | Valida as credenciais do IPBeja |

> **Ator abstrato** — nunca interage diretamente com o sistema por si só. Define comportamentos partilhados que são herdados pelos atores concretos através de generalização.  
> **Ator primário** — inicia interações com o sistema para atingir um objetivo próprio.  
> **Ator secundário** — é chamado pelo sistema para fornecer um serviço; não inicia a interação.

---

## Relação de Generalização

```
Estudante     ──────▷ Utilizador
Administrador ──────▷ Utilizador
```

O ator `Utilizador` agrega os comportamentos comuns a ambos — autenticar-se e recuperar password. Desta forma, evita-se a duplicação de ligações no diagrama de casos de uso e segue-se a boa prática UML de generalização de atores.

---

## Descrição Detalhada

### AT-00 — Utilizador *(abstrato)*

- **Tipo:** Abstrato
- **Descrição:** Ator genérico que representa qualquer pessoa registada e autenticada na plataforma U-Bike. Nunca interage diretamente com o sistema — é sempre através das suas especializações (Estudante ou Administrador).
- **Especializações:** Estudante (AT-01), Administrador (AT-02)
- **Comportamentos herdados pelos especializados:**
  - Autenticar-se (UC-02)
  - Recuperar password (UC-03)

---

### AT-01 — Estudante

- **Tipo:** Primário (especialização de Utilizador)
- **Descrição:** Membro da comunidade académica do IPBeja registado na plataforma. É o utilizador principal do serviço de bicicletas partilhadas.
- **Motivação:** Utilizar bicicletas do IPBeja de forma cómoda, monitorizar os seus percursos e acompanhar os seus indicadores de saúde e eficiência energética.
- **Pré-condições de acesso:** Ter conta registada e autenticada com credenciais institucionais.
- **Interações principais com o sistema:**
  - Registar-se (UC-01) *(exclusivo do Estudante)*
  - Autenticar-se (UC-02) *(herdado de Utilizador)*
  - Recuperar password (UC-03) *(herdado de Utilizador)*
  - Reservar uma bicicleta (UC-04)
  - Cancelar uma reserva (UC-05)
  - Iniciar e terminar um percurso (UC-06, UC-07)
  - Devolver uma bicicleta (UC-08)
  - Consultar histórico de percursos (UC-09)
  - Consultar indicadores pessoais (UC-10)
  - Editar perfil (UC-11)

---

### AT-02 — Administrador

- **Tipo:** Primário (especialização de Utilizador)
- **Descrição:** Membro do staff do IPBeja responsável pela gestão operacional do projeto U-Bike. A sua conta é criada diretamente no sistema — não se regista através da plataforma.
- **Motivação:** Garantir o bom funcionamento da frota, gerir utilizadores e monitorizar o uso global do sistema.
- **Pré-condições de acesso:** Ter conta com perfil de administrador criada pelo sistema e estar autenticado.
- **Interações principais com o sistema:**
  - Autenticar-se (UC-02) *(herdado de Utilizador)*
  - Recuperar password (UC-03) *(herdado de Utilizador)*
  - Gerir utilizadores (UC-12)
  - Gerir frota de bicicletas (UC-15)
  - Consultar relatórios globais (UC-16)
  - Consultar indicadores agregados (UC-17)
  - Configurar parâmetros do sistema (UC-18)

> **Nota:** O Administrador **não tem acesso** ao UC-01 (Registar-se). A sua conta é criada internamente por outro administrador ou via configuração do sistema.

---

### AT-03 — Sistema GPS / Monitorização

- **Tipo:** Secundário (ator externo)
- **Descrição:** Representa o conjunto de sensores e hardware embebido nas bicicletas (GPS, sensores de velocidade e distância) que comunica com a plataforma em tempo real durante os percursos.
- **Motivação:** Não tem motivação própria — é chamado pela plataforma para fornecer dados de localização e telemetria durante um percurso ativo.
- **Pré-condições de acesso:** Bicicleta em utilização com percurso iniciado.
- **Interações principais com o sistema:**
  - Registar dados de percurso (UC-14)

> **Nota:** Para efeitos deste projeto, o Sistema GPS pode ser simulado através de dados introduzidos manualmente ou gerados automaticamente pela plataforma, caso não exista hardware físico disponível.

---

### AT-04 — Sistema de Autenticação Institucional

- **Tipo:** Secundário (ator externo)
- **Descrição:** Representa o serviço de autenticação do IPBeja que valida as credenciais dos utilizadores via API. A plataforma U-Bike delega a verificação de identidade neste sistema.
- **Motivação:** Não tem motivação própria — é invocado sempre que um utilizador tenta autenticar-se ou recuperar a password na plataforma.
- **Pré-condições de acesso:** Utilizador com credenciais institucionais válidas (@ipbeja.pt).
- **Interações principais com o sistema:**
  - Autenticar-se (UC-02)
  - Recuperar password (UC-03)

---

## Diagrama de Generalização

```
          ┌─────────────┐
          │  Utilizador │  ← abstrato
          └──────┬──────┘
        ┌────────┴────────┐
        ▼                 ▼
  ┌──────────┐     ┌───────────────┐
  │ Estudante│     │ Administrador │
  └──────────┘     └───────────────┘
```

---

## Referências

- Enunciado do Trabalho Prático — Engenharia de Software 2025/2026
- UML 2.5 — Use Case Diagrams: https://www.uml-diagrams.org/use-case-diagrams.html
