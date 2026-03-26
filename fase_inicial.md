# Recolha e Análise de Informação

## Métodos de recolha

Para perceber como funcionam os sistemas de empréstimo de bicicletas em contexto académico, utilizámos as seguintes formas de obtenção de informação:

- Pesquisa online dos sistemas U-Bike já existentes noutras instituições de ensino superior, nomeadamente IPLeiria, IPBeja e IPBragança.
- Análise dos regulamentos de utilização publicados por cada instituição.
- Consulta das descrições das aplicações móveis nas lojas App Store e Google Play.
- Comparação entre os vários sistemas para perceber o que é comum e o que difere entre eles.

## Fontes consultadas

- U-Bike IPBeja — Como Funciona: https://www.ipbeja.pt/sas/gaad/U-Bike/Paginas/ComoFunciona.aspx
- U-Bike IPBeja — Site do projeto: https://bika4.webnode.pt/
- U-Bike IPLeiria — Página oficial: https://www.ipleiria.pt/en/live/student-life/u-bike/
- IPBike (IPBragança): http://ipbike.ipb.pt/PT_ipbike.html
- Portal Alentejano — U-Bike IPBeja: https://www.portalalentejano.com/projeto-u-bike-ipbeja/

## O que descobrimos

### Modelo geral de funcionamento

Verificámos que o modelo U-Bike não funciona como um sistema de partilha rápida tipo Gira de Lisboa. É um empréstimo de longa duração — o estudante candidata-se, celebra um contrato com a instituição, recebe uma bicicleta e fica com ela durante 6 a 12 meses. No final desse período, devolve-a.

O processo segue sempre a mesma lógica: candidatura, seleção com base em critérios do regulamento, assinatura de contrato e seguro, entrega da bicicleta, utilização com monitorização, e devolução no final do contrato.

### U-Bike IPBeja

No IPBeja, as bicicletas são propriedade da instituição e destinam-se exclusivamente à comunidade académica. A utilização está restrita ao concelho de Beja. A entrega é feita presencialmente no Gabinete de Apoio à Atividade Desportiva (GAAD) após assinatura de contrato e aquisição de seguro. O uso é intransmissível — o estudante não pode emprestar a bicicleta a ninguém. O mínimo exigido é de cerca de 2000 metros por dia, o que dá aproximadamente 60 km por mês.

### U-Bike IPLeiria

O sistema do IPLeiria é o mais completo em termos digitais e serviu-nos como principal referência. Tem uma aplicação móvel que permite desbloquear a bicicleta diretamente pelo telemóvel, consultar um mapa em tempo real com as estações e a disponibilidade de bicicletas, ver o histórico de viagens com distâncias e tempos percorridos, controlar o tempo de viagem com um temporizador e alertas, verificar o nível de bateria nas bicicletas elétricas, reportar problemas diretamente pela app e aceder ao perfil de utilizador. As bicicletas estão equipadas com um sistema de georeferenciação GPS em tempo real. Os dados recolhidos são anónimos, em conformidade com o RGPD. O mínimo exigido é de 40 km por mês, com contratos de 6 meses.

### IPBike (IPBragança)

No IPBragança encontrámos alguns aspetos que complementam os anteriores. O registo de adesão é feito pela internet e pode ser feito durante todo o ano. Quando o estudante é selecionado, tem 48 horas para levantar a bicicleta. Existe um sistema de caução — o estudante paga um valor inicial que só é devolvido na totalidade se cumprir os km mínimos. A monitorização dos km é feita mensalmente na área de utilizador. A manutenção é agendada pelo sistema e registada na plataforma pela empresa que faz a assistência. Se houver danos por negligência, os custos são da responsabilidade do utilizador.

### Porquê os km mínimos?

Um aspeto que nos pareceu importante perceber foi a razão de existirem km mínimos obrigatórios. Concluímos que isto se deve ao facto de o projeto ter sido financiado com fundos europeus (programa POSEUR). Para justificar esse investimento público, as instituições precisam de demonstrar que as bicicletas estão realmente a ser usadas e que existe impacto ambiental mensurável. Além disso, como as bicicletas são um recurso limitado, os km mínimos garantem que só fica com a bicicleta quem efetivamente a utiliza, libertando-a para outro estudante caso contrário.

## Conclusão da análise inicial

Com base nesta pesquisa, percebemos que a plataforma que vamos modelar precisa de cobrir dois pontos de vista, tal como indicado no enunciado: o do fornecedor do serviço (a instituição que gere as bicicletas) e o de quem usufrui (o estudante). Decidimos usar o sistema do IPLeiria como referência principal para as funcionalidades digitais, complementando com os mecanismos de caução e manutenção do IPBragança e as regras específicas do IPBeja.

Os dois indicadores exigidos no enunciado — eficiência energética e hábitos de vida saudáveis — dependem diretamente dos dados de utilização. A eficiência energética mede a poupança de combustível e CO2 por usar a bicicleta em vez do carro. Os hábitos saudáveis medem o exercício realizado: calorias, distância e tempo ativo. Ambos serão alimentados pelos dados GPS recolhidos durante as viagens.