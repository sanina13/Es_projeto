# Recolha e Análise de Informação

## Métodos de recolha

Para perceber como funcionam os sistemas de empréstimo de bicicletas em contexto académico, utilizámos as seguintes formas de obtenção de informação:

- Pesquisa online dos sistemas U-Bike já existentes noutras instituições de ensino superior, nomeadamente IPLeiria, IPBeja e IPBragança.
- Análise dos regulamentos de utilização publicados por cada instituição.
- Consulta das descrições das aplicações móveis nas lojas App Store e Google Play.
- Consulta da documentação oficial do programa POSEUR no portal Portugal 2020.
- Comparação entre os vários sistemas para perceber o que é comum e o que difere entre eles.

## Fontes consultadas

- U-Bike IPBeja — Como Funciona: https://www.ipbeja.pt/sas/gaad/U-Bike/Paginas/ComoFunciona.aspx
- U-Bike IPBeja — Site do projeto: https://bika4.webnode.pt/
- U-Bike IPLeiria — Página oficial (em inglês): https://www.ipleiria.pt/en/live/student-life/u-bike/
- IPBike (IPBragança) — Regras e funcionamento: http://ipbike.ipb.pt/PT_ipbike.html
- IPBragança — Ficha do projeto no Portugal 2020: https://transparencia.gov.pt/pt/fundos-europeus/pt2020/beneficiarios-projetos/projeto/POSEUR-01-1407-FC-000010/
- POSEUR — Notícia sobre o projeto U-Bike Portugal: https://poseur.portugal2020.pt/pt/media/noticias/projeto-u-bike-disponibiliza-mais-de-tres-mil-bicicletas-ao-ensino-superior/
- Portal Alentejano — U-Bike IPBeja: https://www.portalalentejano.com/projeto-u-bike-ipbeja/

## O que descobrimos

### Contexto geral do programa U-Bike Portugal

O projeto U-Bike Portugal é uma iniciativa nacional, coordenada pelo Instituto da Mobilidade e dos Transportes (IMT), financiada pelo POSEUR (Programa Operacional Sustentabilidade e Eficiência no Uso de Recursos) no âmbito do Portugal 2020. O investimento total ultrapassou os 6 milhões de euros, dos quais cerca de 4,7 milhões vieram do Fundo de Coesão da União Europeia. O projeto teve início em setembro de 2016 e abrangeu 15 instituições de ensino superior.

No total, foram adquiridas 3.234 bicicletas — 2.096 elétricas e 1.138 convencionais — distribuídas pelas comunidades académicas de 26 municípios. O objetivo era que fossem percorridos mais de 2.412.141 km por ano em bicicleta, o que corresponderia a uma poupança estimada de 166,34 toneladas equivalentes de petróleo (tep) e a uma redução de 505 toneladas equivalentes de CO2.

### Modelo geral de funcionamento

Verificámos que o modelo U-Bike não funciona como um sistema de partilha rápida tipo Gira de Lisboa. É um empréstimo de longa duração — o estudante candidata-se, celebra um contrato com a instituição, recebe uma bicicleta e fica com ela durante 6 a 12 meses. No final desse período, devolve-a.

O processo segue sempre a mesma lógica geral em todas as instituições: candidatura, seleção com base em critérios definidos no regulamento, assinatura de contrato e seguro, entrega da bicicleta, utilização com monitorização de km, e devolução no final do contrato.

### U-Bike IPBeja

No IPBeja, as bicicletas são propriedade da instituição e destinam-se ao uso exclusivo da comunidade académica, tanto para deslocações de lazer como de trabalho. A utilização está restrita à área geográfica do concelho de Beja, conforme o regulamento.

A candidatura é feita através de um formulário online, em períodos definidos pela coordenação do projeto (existem também candidaturas fora desses períodos). As candidaturas são analisadas e seriadas com base nos critérios do Regulamento de Utilização de Bicicletas.

A entrega da bicicleta é feita presencialmente no Gabinete de Apoio à Atividade Desportiva (GAAD), após a celebração de um contrato escrito e a aquisição de um seguro. O uso é intransmissível — o estudante não pode emprestar, alugar ou ceder a bicicleta a terceiros.

O utilizador compromete-se a realizar deslocações regulares de e para o campus, em média 2000 metros por dia, num mínimo de 60 km mensais. Os contratos têm duração de 6 a 12 meses.

### U-Bike IPLeiria

O IPLeiria desenvolveu o sistema mais completo em termos de funcionalidades digitais, tendo sido criada uma aplicação móvel pela empresa Bewegen/Wegoshare. Segundo a descrição disponível no site oficial e nas lojas de aplicações, a app permitia: desbloquear a bicicleta diretamente pelo telemóvel (ou em alternativa pelo cartão institucional), consultar um mapa em tempo real com as estações e a disponibilidade de bicicletas, ver o histórico de viagens com rotas, distâncias e tempos percorridos, controlar o tempo de viagem com um temporizador e alertas, verificar o nível de bateria nas bicicletas elétricas, reportar problemas diretamente pela app e aceder ao perfil de utilizador. As bicicletas estão equipadas com um sistema de georeferenciação e comunicação em tempo real que regista o percurso e os km realizados. Os dados recolhidos são anónimos, em conformidade com a legislação de proteção de dados.

O mínimo exigido é de 40 km por mês, com contratos de 6 meses. As candidaturas estão abertas a toda a comunidade académica, desde que o candidato confirme que possui carta de condução, se desloque regularmente para o campus em veículos motorizados a combustível fóssil e se comprometa a cumprir os km mínimos.

No entanto, ao tentarmos testar a aplicação, verificámos que a última atualização no Android (Google Play) data de agosto de 2022, que a página da App Store (iOS) retorna erro 404 e que a app não aparece em pesquisas no iPhone. Isto indica que a componente digital do projeto poderá já não estar ativa ou ter sido descontinuada. Assim, utilizámos a descrição das funcionalidades como referência para a modelação da nossa plataforma, mas tendo consciência de que se trata de um sistema que aparenta estar desatualizado.

### IPBike (IPBragança)

No IPBragança encontrámos um sistema bem documentado com aspetos que complementam os anteriores. O registo de adesão é feito pela internet e pode ser realizado durante todo o ano por qualquer membro da comunidade académica. Quando o estudante é selecionado, é avisado por email ou telemóvel e tem 48 horas para efetuar o levantamento da bicicleta e do respetivo kit.

No ato do levantamento são assinados um contrato de utilização e um termo de responsabilidade. O utilizador é totalmente responsável pela bicicleta durante o período contratualizado (6 a 12 meses).

O sistema de caução é um aspeto diferenciador: o estudante paga uma caução de 80 euros no início e, adicionalmente, 20 euros mensais para seguro e manutenção. Se não cumprir os km contratualizados, a caução não é devolvida na totalidade. Os utilizadores comprometem-se a permitir o registo mensal do número de km na área de utilizador do projeto.

A manutenção é agendada pelo sistema e as bicicletas só podem ser assistidas no local indicado pelo IPB, nas datas marcadas na área de utilizador. A empresa responsável pela manutenção regista na plataforma os trabalhos realizados e o número de km do período em causa. Se houver necessidade de manutenção corretiva por avaria, o pedido é feito na área de utilizador e carece de autorização prévia. Os custos de reparações por negligência são da responsabilidade do utilizador.

Consultámos também a ficha do projeto do IPBragança no portal Portugal 2020, que descreve as funcionalidades previstas para a plataforma: registo individual, reserva de bicicleta, comunicação de situações irregulares (avaria, dano ou furto), indicação de km e calorias gastas, agendamento de manutenções, pagamento online de cauções e seguros. Do lado do backoffice (gestão), a plataforma permitiria gestão de utilizadores, registo e gestão de bicicletas, consulta de km totais e mensais, controlo de manutenções e gestão de pagamentos. A plataforma também disponibilizaria ao público informação sobre km totais e estimativas de redução de CO2.

### Porquê os km mínimos?

Um aspeto que nos pareceu importante perceber foi a razão de existirem km mínimos obrigatórios em todas as instituições. Concluímos que isto se deve a vários fatores:

Primeiro, o projeto foi financiado com fundos europeus. Para justificar o investimento público de mais de 6 milhões de euros, as instituições precisam de demonstrar que as bicicletas estão realmente a ser usadas e que existe impacto ambiental mensurável — os tais 2,4 milhões de km/ano e as 505 toneladas de CO2 evitadas.

Segundo, as bicicletas são um recurso limitado. O IPBeja, por exemplo, não tem bicicletas para toda a comunidade académica. Os km mínimos garantem que só fica com a bicicleta quem efetivamente a utiliza, libertando-a para outro estudante caso contrário.

Terceiro, o mecanismo de caução (como no IPBragança) funciona como incentivo financeiro ao cumprimento.

## Conclusão da análise inicial

Com base nesta pesquisa, percebemos que a plataforma que vamos modelar precisa de cobrir dois pontos de vista, tal como indicado no enunciado: o do fornecedor do serviço (a instituição que gere as bicicletas) e o de quem usufrui (o estudante).

Decidimos usar como referência principal a lista de funcionalidades prevista para a plataforma do IPBragança (descrita na ficha do Portugal 2020), uma vez que é a mais detalhada e documentada oficialmente. Complementámos com as funcionalidades digitais descritas na app do IPLeiria (mesmo estando aparentemente descontinuada, a descrição das features continua a ser relevante) e com as regras específicas do IPBeja, que é a instituição do nosso contexto.

Os dois indicadores exigidos no enunciado — eficiência energética e hábitos de vida saudáveis — dependem diretamente dos dados de utilização. A eficiência energética mede a poupança de combustível e CO2 por usar a bicicleta em vez do carro. Os hábitos saudáveis medem o exercício realizado: calorias, distância e tempo ativo. Ambos serão alimentados pelos dados de km recolhidos durante as viagens.