# Requisitos Funcionais — Plataforma U-Bike IPBeja

> **Prioridade:** Alta (sistema não funciona sem este RF) · Média (importante mas não crucial) · Baixa (melhoria/inovação)

| ID | Descrição | Ator | Prioridade |
|----|-----------|------|------------|
| RF01 | O sistema deve permitir o registo de utilizadores com email institucional (@stu.ipbeja.pt) | Estudante | Alta |
| RF02 | O sistema deve permitir autenticação com email e password | Estudante | Alta |
| RF03 | O sistema deve permitir a recuperação de password através do email institucional | Estudante | Alta |
| RF04 | O sistema deve apresentar um mapa interativo com estações e bicicletas disponíveis em tempo real | Estudante | Alta |
| RF05 | O sistema deve permitir filtrar a pesquisa de bicicletas por tipo (manual ou elétrica) e por estação | Estudante | Alta |
| RF06 | O sistema deve permitir a reserva de uma bicicleta; o utilizador dispõe de 30 minutos para efetuar o levantamento após confirmação da reserva | Estudante | Alta |
| RF07 | O sistema deve garantir que cada utilizador tem no máximo uma reserva ativa em simultâneo | Estudante | Alta |
| RF08 | O sistema deve permitir ao utilizador cancelar uma reserva ativa antes do levantamento da bicicleta | Estudante | Alta |
| RF09 | O sistema deve permitir o desbloqueio da bicicleta via código QR ou NFC | Estudante | Alta |
| RF10 | O sistema deve registar automaticamente a duração, distância e rota GPS de cada viagem | Sistema | Alta |
| RF11 | O sistema deve calcular e apresentar a eficiência energética de cada viagem: kWh/km para bicicletas elétricas e kcal/km para bicicletas manuais | Sistema | Alta |
| RF12 | O sistema deve calcular as calorias consumidas e o CO₂ poupado por viagem, comparando com a deslocação equivalente de carro | Sistema | Alta |
| RF13 | O sistema deve permitir a devolução da bicicleta em qualquer estação da rede com lugar disponível; se a estação estiver cheia, o sistema deve sugerir a estação alternativa mais próxima | Estudante | Alta |
| RF14 | O sistema deve enviar notificações por email em eventos críticos: confirmação de reserva, lembrete 10 minutos antes da expiração e alerta de devolução | Sistema | Alta |
| RF15 | O sistema deve enviar notificações push na aplicação em eventos operacionais: desbloqueio, devolução e avaria reportada | Sistema | Média |
| RF16 | O sistema deve apresentar o histórico de viagens do utilizador com métricas detalhadas por viagem | Estudante | Média |
| RF17 | O sistema deve disponibilizar um dashboard de saúde com estatísticas acumuladas (distância total, calorias totais, CO₂ total poupado) | Estudante | Média |
| RF18 | O sistema deve permitir ao utilizador reportar avarias ou danos nas bicicletas, com descrição e fotografia opcional | Estudante | Média |
| RF19 | O administrador deve poder gerir a frota de bicicletas (adicionar, atualizar estado e remover bicicletas) | Admin | Alta |
| RF20 | O administrador deve poder gerir as estações (adicionar, editar localização e capacidade, remover) | Admin | Alta |
| RF21 | O administrador deve poder visualizar estatísticas de uso em tempo real (bicicletas em uso, disponíveis, em manutenção) | Admin | Alta |
| RF22 | O administrador deve poder gerar relatórios exportáveis (PDF/CSV) de uso, eficiência energética e indicadores de saúde | Admin | Média |
| RF23 | O sistema deve monitorizar o nível de bateria das bicicletas elétricas e alertar o administrador quando inferior a 20% | Sistema | Média |
| RF24 | O administrador deve poder agendar manutenção preventiva das bicicletas, ficando estas indisponíveis para reserva durante o período agendado | Admin | Média |
| RF25 | O sistema deve gerir o processo de candidatura e aprovação de novos utilizadores, notificando o estudante do resultado | Admin | Média |
| RF26 | O sistema deve incluir um sistema de gamificação com atribuição de pontos por viagem e ranking entre utilizadores | Estudante | Baixa |




| 1.1 | 2025-03-28 | sanina13 | Correções: prioridades, RF07 energia, RF06 reserva, RF10 notificações separadas; adicionados RF03, RF05, RF07 (limite reservas), RF08 (cancelar), RF20 (estações) |

