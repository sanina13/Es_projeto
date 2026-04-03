# Atores do Sistema — Plataforma U-Bike

**Projeto:** U-Bike IPBeja  
**UC:** Engenharia de Software 2025/2026  
**Fase:** Análise — Casos de Uso  

---

## Visão Geral

O sistema U-Bike envolve **4 atores**, divididos em dois tipos:

| Tipo | Ator | Descrição resumida |
|------|------|--------------------|
| Primário | Estudante | Utilizador principal da plataforma |
| Primário | Administrador | Gestor da frota e da plataforma |
| Secundário | Sistema GPS / Monitorização | Fornece dados de localização e percurso |
| Secundário | Sistema de Autenticação Institucional | Valida as credenciais do IPBeja |

> **Ator primário** — inicia interações com o sistema para atingir um objetivo próprio.  
> **Ator secundário** — é chamado pelo sistema para fornecer um serviço; não inicia a interação.

---

## Descrição Detalhada

### AT-01 — Estudante

- **Tipo:** Primário  
- **Descrição:** Membro da comunidade académica do IPBeja (estudante, docente ou funcionário) registado na plataforma. É o utilizador principal do serviço de bicicletas partilhadas.  
- **Motivação:** Utilizar bicicletas do IPBeja de forma cómoda, monitorizar os seus percursos e acompanhar os seus indicadores de saúde e eficiência energética.  
- **Pré-condições de acesso:** Ter conta registada e autenticada com credenciais institucionais.  
- **Interações principais com o sistema:**
  - Registar-se na plataforma
  - Autenticar-se
  - Reservar uma bicicleta
  - Cancelar uma reserva
  - Iniciar e terminar um percurso
  - Devolver uma bicicleta
  - Consultar histórico de percursos
  - Consultar indicadores pessoais (calorias, distância, CO₂ poupado)

---

### AT-02 — Administrador

- **Tipo:** Primário  
- **Descrição:** Membro do staff do IPBeja responsável pela gestão operacional do projeto U-Bike. Tem acesso a funcionalidades de gestão que não estão disponíveis para o Estudante.  
- **Motivação:** Garantir o bom funcionamento da frota, gerir utilizadores e monitorizar o uso global do sistema.  
- **Pré-condições de acesso:** Ter conta com perfil de administrador e estar autenticado.  
- **Interações principais com o sistema:**
  - Autenticar-se
  - Gerir utilizadores (listar, ativar, desativar)
  - Gerir frota de bicicletas (adicionar, editar, retirar de serviço)
  - Consultar relatórios globais de utilização
  - Consultar indicadores agregados (eficiência energética, hábitos de saúde)
  - Configurar parâmetros do sistema

---

### AT-03 — Sistema GPS / Monitorização

- **Tipo:** Secundário (ator externo)  
- **Descrição:** Representa o conjunto de sensores e hardware embebido nas bicicletas (GPS, sensores de velocidade e distância) que comunica com a plataforma em tempo real durante os percursos.  
- **Motivação:** Não tem motivação própria — é chamado pela plataforma para fornecer dados de localização e telemetria durante um percurso ativo.  
- **Pré-condições de acesso:** Bicicleta em utilização com percurso iniciado.  
- **Interações principais com o sistema:**
  - Enviar dados de localização GPS em tempo real
  - Enviar dados de distância percorrida
  - Registar início e fim de percurso
  - Fornecer dados para cálculo de eficiência energética e indicadores de saúde

> **Nota:** Para efeitos deste projeto, o Sistema GPS pode ser simulado através de dados introduzidos manualmente ou gerados automaticamente pela plataforma, caso não exista hardware físico disponível.

---

### AT-04 — Sistema de Autenticação Institucional

- **Tipo:** Secundário (ator externo)  
- **Descrição:** Representa o serviço de autenticação do IPBeja (ex: LDAP ou SSO institucional) que valida as credenciais dos utilizadores. A plataforma U-Bike delega a verificação de identidade neste sistema.  
- **Motivação:** Não tem motivação própria — é invocado sempre que um utilizador tenta autenticar-se na plataforma.  
- **Pré-condições de acesso:** Utilizador com credenciais institucionais válidas (email @stu.ipbeja.pt ou @ipbeja.pt).  
- **Interações principais com o sistema:**
- Validar credenciais do utilizador (email + password)
- Confirmar identidade para autorizar acesso à plataforma

## Referências

- Enunciado do Trabalho Prático — Engenharia de Software 2025/2026
