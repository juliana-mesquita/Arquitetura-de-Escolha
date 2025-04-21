# Arquitetura-de-Escolha
<h1> Trabalho da Disciplina de Arquitetura de Escolha - 63ASO </h1>   

<h3> 1. Storytelling sobre o problema </h3>

Durante a pandemia, a empresa de bebidas premium sofreu queda nas vendas. Para reverter o cenário, criou um programa de cashback para incentivar o aumento de vendas. Contudo, o programa apresentou baixa rentabilidade, falta de engajamento dos clientes premium e reclamações dos participantes que achavam as regras do programa confusas. A empresa busca agora transformar essa dor em uma solução digital mais moderna de fidelidade baseada em performance, inteligência de dados e automação dos processos manuais. 

![](https://github.com/juliana-mesquita/Arquitetura-de-Escolha/blob/05d0f9b873ea0e90f4828378dfb5306ae0f52053/storytelling.png)

<h3> 2. O que esperamos aprender com esse projeto? </h3>

- Qual a melhor forma de segmentar clientes e contratos 
- Quais benefícios, incentivos e promoções realmente aumentam o consumo 
- Quais informações os clientes gostariam de ver no Portal 
- Como fazer uma integração com o Salesforce e MTRIX. Funcionamento das suas APIs 

<h3> 3. Que perguntas precisamos que sejam respondidas?</h3>

- Foi realizada alguma pesquisa de mercado para saber a aderência do programa? Se sim, que tipo(s) de pesquisa(s) 
- Qual a taxa estimada de adesão? 
- Quais benefícios a empresa gostaria de oferecer aos clientes no programa? 
- É possível ter apenas um contrato padrão? 
- Quantos pontos em comum existem entre os contratos? 
- Existem um ou mais contratos que podem servir de modelo para a padronização? 
- Foi realizado um estudo financeiro sobre as carteiras de cliente? Se sim, qual? 
- Em quais países a plataforma poderá ser utilizada? 
- Temos mapeadas legislações dos países que pretendemos expandir? Se sim, quais são elas? 
- Dentre os países desejados para a expansão, qual o país com a legislação mais rígida? 
- Há algum histórico de pesquisa de satisfação relacionado à mudanças no programa? 
- Há alguma pesquisa sobre desejos do cliente para o programa de benefício? 
- Quais os critérios para a ativação de promoções sazonais? 
- O período para as campanhas será padrão? 
- Será permitida a criação de campanhas de diversos produtos ao mesmo tempo? 
- As promoções sazonais podem ser acumulativas com outras promoções? 
- As promoções sazonais podem ser acumulativas com o contrato atual do cliente? 
- Quais informações o cliente deseja ter visão? 
- O cliente precisa de uma interface para acompanhamento ou apenas ser notificado? 
- Quais métricas o cliente deseja acompanhar? 
- Será possível realizar a integração com serviços de contratos e notas fiscais?

<h3> 4. Quais são os nossos principais riscos? </h3>

- Baixa adesão dos clientes à nova plataforma 
- Dificuldade na integração com o Sales force e MTRIX 
- Falhas no cálculo automatizado do cashback 
- Dificuldade no enquadramento de clientes aos modelos de fidelização

<h3> 5. Plano para aprender o que precisamos (learning plan): </h3>

Segmentação dos clientes 
- Análise dos dados históricos para identificar padrões e perfis de clientes  
- Realização de entrevistas estruturadas com metodologia Focus group

Segmentação dos contratos 
- Mineração de dados dos contratos atuais para identificar pontos em comum e outliers 
- Benchmarking com programas semelhantes 
  
Definição dos benefícios, incentivos e promoções 
- Co-criação com clientes e validação com áreas de marketing e jurídico 
- Monitoramento dos KPIs das campanhas  
- Análise de comportamento histórico de compra

Informações que os clientes querem ver	 no Portal 
- Design Thinking e entrevistas com clientes  
- Benchmarking com programas semelhantes

Integração com Salesforce e MTRIX 
- Mapeamento dos Sistemas para entender quais dados precisam ser trocados 
- Treinamento da Equipe para aprende as APIs do Salesforce e do MTRIX

<h3> 6. Plano para reduzir riscos: </h3>

- Fase piloto com feedback contínuo. 
- Automação gradual (começar com MVP simples). 
- Monitoramento em tempo real e rollback para regras antigas. 
- Compliance jurídico envolvido desde o início. 
- Treinamento e engajamento dos consultores comerciais. 

<h3> 7. Quem são as partes interessadas? </h3>

- Diretoria comercial e marketing 
- Consultores de vendas 
- Equipe de TI / Produto 
- Clientes finais (bares, distribuidores) 
- Equipe jurídica e compliance

<h3> 8. O que eles esperam ganhar? </h3>

- Diretoria: aumento de vendas e ROI do programa. 
- Consultores: ferramenta fácil de usar e que incentive os clientes. 
- Clientes: benefícios tangíveis, informações claras e facilidade. 
- TI/Produto: arquitetura sustentável e escalável. 
- Equipe jurídica e compliance: padronização dos contratos e segurança

<h3> 9. Quem são os usuários? </h3>

- Clientes (bares, distribuidores) 
- Consultores comerciais e executivos de venda 
- Gestores da empresa

<h3> 10. O que eles estão tentando realizar? </h3>

- Acompanhar performance e ganhos em tempo real. 
- Ser recompensados pelo volume de compras. 
- Planejar campanhas de forma mais estratégica. 
- Gerenciamento eficiente dos contratos

<h3> 11. Qual o pior que pode acontecer? </h3>

- Descontinuidade do programa por baixa adoção ou alto custo. 
- Erros em cashback levando à perda de confiança. 
- Problemas legais e comerciais por contratos mal estruturados.

<h3> 12. Desenho da Arquitetura (Freeform - versão inicial): </h3>

![!](https://github.com/juliana-mesquita/Arquitetura-de-Escolha/blob/a505aa974b656a3638a8c02320e65d4f8c5b6ecd/Arquitetura%20free-form.jpeg)

<h3> 13. Descrição dos componentes: </h3>

<h4> 13.1 Portal do Cliente </h4>

- Interface web responsiva e aplicativo móvel para acesso omnichannel 
- Autenticação multi-fator com níveis de acesso (visualização, administrador, etc.) 
- Funcionalidades principais: 
  - Visualização detalhada de contratos ativos/inativos 
  - Histórico de consumo com filtros e exportação de dados 
  - Extrato de cashback (disponível, utilizado, a receber) 
  - Área de resgate/utilização do cashback 
  - Notificações personalizáveis (email, SMS, push) 
  - Documentação fiscal (notas fiscais, recibos) 
- Seção de ajuda com FAQ, tutoriais e chat de suporte 
- Área de feedback do cliente para melhoria contínua 
- Analytics de comportamento do usuário integrado 

<h4> 13.2 Motor de Regras </h4>

- Sistema parametrizável baseado em políticas de negócio 
- Algoritmos para cálculo dinâmico de cashback considerando: 
  - Perfil do cliente (segmento, histórico) 
  - Volume e recorrência de compras 
  - Sazonalidade e campanhas promocionais 
  - Categorias de produtos/serviços 
  - Fidelidade (tempo de relacionamento) 
- Versionamento de regras com histórico de mudanças 
- Capacidade de simulação para testar impacto de novas regras 
- API documentada para integração com outros sistemas 
- Logs detalhados para auditoria e rastreabilidade 
- Processamento em tempo real e batch para diferentes cenários 
- Interface administrativa para configuração de regras sem necessidade de código

<h4>13.3 ETL/Stream (Integração) </h4>

- Arquitetura de mensageria baseada em Apache Kafka 
- Conectores específicos para Sales force e MTRIX com transformação de dados em tempo real 
- Camadas de integração: 
  - Captura de dados (CDC) do banco operacional 
  - Transformação e enriquecimento 
  - Carregamento em sistemas-alvo 
- Processamento de eventos complexos (CEP) para detecção de padrões 
- Mecanismos de retry e dead-letter queue para tratamento de falhas 
- Monitoramento de latência e throughput 
- Governança de dados com validação e qualidadeSincronização bidirecional entre sistemas 
- Rastreabilidade completa do fluxo de dados 
- Módulo de reconciliação para garantir consistência

<h4> 13.4 Dashboard BI </h4>

- Plataforma de Business Intelligence com diferentes visões: 
  - Visão executiva (KPIs principais, tendências) 
  - Visão operacional (indicadores diários, alertas) 
  - Visão analítica (análises ad-hoc, drill-down)
- Métricas principais: 
  - Análise de adesão ao programa de cashback 
  - Taxa de utilização do cashback disponível 
  - Impacto nas vendas e retenção 
  - Segmentação de clientes por comportamento 
  - ROI das campanhas de cashback
- Recursos avançados: 
  - Análise preditiva de comportamento futuro 
  - Alertas automáticos para desvios significativos 
  - Exportação programada de relatórios 
  - Dashboards personalizáveis por perfil de usuário 
  - Integração com ferramentas de BI externas (Power BI, Tableau, etc.)
- Histórico comparativo e análise de tendências 

<h4> 13.5 Simulador de Cashback </h4>

- Ferramenta interativa com duas interfaces: 
  - Versão para consultores (mais detalhada, com acesso a cenários complexos) 
  - Versão para clientes (simplificada, intuitiva) 
- Funcionalidades: 
  - Simulação baseada em produtos/serviços específicos 
  - Comparação lado a lado de diferentes cenários 
  - Projeção de economias ao longo do tempo 
  - Recomendação de mix ideal de produtos/serviços 
  - Geração de propostas/cotações baseadas na simulação 
- Integração com o CRM para registro de oportunidades 
- Incorporação de histórico do cliente para simulações personalizadas 
- Exportação do resultado em PDF/Excel para apresentações 
- Versionamento das simulações para acompanhamento 
- API para integração com outros canais de vendas 
- Feedback em tempo real das regras aplicadas na simulação

<h4> 13.6 Banco de Dados e Armazenamento (Componente adicional) </h4>

- Arquitetura híbrida: 
  - Banco relacional para transações (PostgreSQL/Oracle) 
  - Banco NoSQL para análises e dados não estruturados (MongoDB/Cassandra)
- Data Lake em três camadas (bronze, silver, gold)Modelos de dados: 
  - Contratos (termos, condições, histórico de alterações) 
  - Transações (compras, resgates, estornos) 
  - Cashback (acumulado, disponível, expirado) 
  - Perfil e comportamento do cliente 
- Políticas de retenção e arquivamento 
- Esquema de particionamento para performance 
- Redundância geográfica para alta disponibilidade 
- Criptografia de dados sensíveis 
- Mecanismos de backup e recovery

<h4> 13.7 Serviço de Notificações (Componente adicional) </h4>

- Sistema centralizado de comunicação multicanal: 
  - Email (templates personalizáveis) 
  - SMS (mensagens compactas) 
  - WhatsApp (mensagens ricas, interativas) 
  - Push notifications (app móvel) 
- Tipos de notificações: 
  - Transacionais (confirmações, alertas) 
  - Informativas (novos benefícios, atualizações) 
  - Marketing (ofertas personalizadas baseadas em perfil) 
  - Operacionais (manutenção, alterações de regras) 
- Motor de personalização baseado em preferências do usuário 
- Agendamento e priorização de mensagens 
- Analytics de taxas de abertura e engajamento 
- Sistema de opt-in/opt-out conforme regulamentações 
- Testes A/B para otimização de mensagens

<h4> 14. Requisitos importantes: </h4>

- Integração automática com Salesforce e MTRIX. 
- Cálculo em tempo real do cashback. 
- Portal com visibilidade clara para o cliente. 
- Flexibilidade para criar promoções sazonais. 
- Alta disponibilidade e segurança de dados. 
