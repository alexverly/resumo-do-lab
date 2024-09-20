# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO
# O que eu aprendi?
Nesse lab aprendi sobre algumas categorias dentro do Portal Azure e como serão importantes nos próximos passos do curso.
# Criando Máquinas Virtuais na Azure
Benefícios da nuvem
- domínio de objetivo
-- Descrever os benefícios de alta disponibilidade e da escalabilidade na nuvem
-- Descrever os benefícios da confiabilidade e da previsibilidade na nuvem
-- Descrever os benefícios da segurança e da governança na nuvem
-- Descrever os benefícios da capacidade de gerenciamento na nuvem

Alta disponibilidade
- recursos disponíveis sempre que forem necessários
- SLA: Service Level Agreement
- Alta disponibilidade se concentra em garantir o máximo possível de disponibilidade, independentemente de interrupções ou eventos que possam ocorrer

Escalabilidade
- A escalabilidade refere-se à capacidade de ajustar recursos para atender à demanda
- A capacidade de escalar significa que você poderá adicionar mais recursosm para lidar melhor com o aumento da demanda
- O outro benefício da escalabilidade é que você não está pagando além do necessário pelos serviços
- Como a nuvem é um modelo baseado em consumo, você paga apenas pelo que usa.
- Se a demanda cair, você poderá reduzir seus recursos e, assim, reduzir seus custos
- Com a escala vertical, se você estivesse desenvolvendo um aplicativo e precisasse de mais capacidade de processamento, poderia escalar verticalmente para adicionar mais CPUs ou RAM à máquina virtual

Elasticidade
- Com a elasticidade, se você experimentasse um salto repentino acentuado na demanda, seus recursos implantados poderiam ser expandidos (automaticamente ou manualmente)
- Por exemplo, você pode adicionar máquinas virtuais ou contêineres por meio da expansão.
- Da mesma forma, se houver uma queda significativa de demanda, os recursos implantados poderão ser reduzidos horizontalmente (de maneira automática ou manual).

Confiabilidade
- Devido ao design descentralizado, a nuvem naturalmente dá suporte a uma infraestrutura confiável e resiliente
- Com um design descentralizado, a nuvem permite que você tenha recursos implantados em várias regiões do mundo
- Com essa escala global, mesmo que ocorra um evento catástrófico em uma região, as outras regiões ainda estarão em funcionamento

Previsibilidade
- A previsibilidade na nuvem permite que você avance com confiança, seja no desempenho ou no custo. Ambas são influenciadas pelo Microsoft Azure Well-Architected Framework

Segurança
- A nuvem oferece ferramentas de segurança que atendem às necessidades dos clientes mas, é importante lembrar que a implementação de muitas delas devem ser realkizadas pelo cliente
- Se você quiser o controle máximo da segurança, a infraestrutura como serviço fornecerá recursos fisicos, mas permitirá que você gerencie os sistemas operacionais e o software instalado, incluindo aplicação de patches e manutenção

Governança
- A auditoria baseada em nuvem ajuda a sinalizar qualquer recurso que esteja fora de conformidade com seus padrões corporativos e fornece estratégias de mitigação

Gerenciabilidade
- Um dos principais benefícios da computação em nuvem são as opções de capacidade de gerenciamento. Há dois tipos de capacidade de gerenciamento para computação em nuvem que você aprenderá nesta série e ambos trazem excelentes benefícios
- O gerenciamento da nuvem diz respeito a gerenciar seus recursos de nuvem. Por exemplo: Escalar automaticamente a implantação de recursos com base na necessidade
- Implantar recursos com base em um modelo pré-configurado, removendo a necessidade de configuração manual
- O gerenciamento na nuvem diz respeito à maneira de gerenciar seu ambiente de nuvem e seus recursos. Por exemplo:
- Por meio de um portal da Web
- Usando uma interface de linha de comando
- Usando APIs
- Usando o PowerShell

SLA / Tempo

- 99% -> 1,68h/senama -> 7,2h/mês -> 3,65dias/ano
- 99,9% -> 10,1min/semana -> 43,2 min/mês -> 8,76h/ano
- 99,95% -> 5min/semana -> 21,6min/mês -> 4,38h/ano
- 99,999% -> 6 seg/semana -> 25,9seg/mês -> 5,26/ano

# Tipos de Serviço de Nuvem
- Descrever o modelo de responsabilidade compartilhada
- Identificar os casos de uso apropriados para cada serviço de nuvem (IaaS, PaaS e SaaS)
- As diferenças estão no licenciamento
- O ambiente on-promise é de total responsabilidade do cliente

IaaS (Infrastructure as a Service)
- É o mais utilizado
- Recursos que temos acesso, onde configuramos
- Crie uma infraestruturade TI de pagaemnto conforme o uso alugando servidores, máquinas virtuais, armazenamento, redes e sistemas operacionais de um provedor de nuvem.
- É o mais flexível, te dá mais poder de gerenciar
- Você configura e gernecia para o seu aplicativo
- Maior gestão

PaaS (Platform as a Service)
- Engloba IaaS (adicionando Sistemas Operacionais e Ferramentas para desenvolvedores, análise de negócios de gerenciamento de database)
- Fornece um ambiente para a criação, o teste e a implantação de aplicativos de software, sem focar no gerenciamento da infraestrutura subjacente.
- Focado no desenvolvimento de aplicativos- O gerenciamento de plataforma é realizado pelo provedor de nuvem
- Gestão intermediária
- Os usuários podem criar e implantar um aplicativo o mais rápido possível, sem terem que se preocupar com gerenciar a infraestrutura subjacente

SaaS (Software as a Service)
- Engloba IaaS e PaaS
- Aplicativos e Apps hospedados
- Modelo de preço de pagamento conforme uso
- Os usuários pagam pelo software que utilizam em um modelo de assinatura
- Menor gestão

Hands-on / Configurando uma instância de Banco de Dados na Azure

# Componentes de Arquitetura de Azure

Objetivos
- Descrever regiões, pares de regiões e regiões soberanas do Azure
- Descrever as zonas de disponibilidade
- Descrever os datacenters do Azure
- Descrever os recursos e os grupos de recursos do Azure
- Descrever as assinaturas
- Descrever os grupos de gerenciamento
- Descrever a hierarquia de grupos de recursos, assinaturas e grupos de gerenciamento

Contas do Azure
- Conta do Azure
- Conta gratuita do Azure
- Conta de estudante gratuita do Azure
- Área restrita do Microsoft Learn

Regiões / Zona de Disponibilidade
- O Azure oferece mais regiões globais do que qualquer outro provedor de nuvem, com mais de 60 regiões representando mais de 140 países
- As regiões são compostas de um ou mais datacenters muito próximos
- Eles fornecem flexibilidade e escala para reduzir a latência do cliente (Redundância?)
- As regiões preservam a residência dos dados com uma oferta abrangente de conformidade (LGPD?)
- Fornece proteção contra tempo de inatividade devido a falha do datacenter
- Separe fisicamente os datacenters dentro da mesma região
- Cada datacenter é equipado com alimentação, resfriamento e rede independentes
- Conectadas por meio de redes privadas de fibra óptica

# Entendendo Pares de Região e Grupos de Recursos

Pares de Regiões
- No mínimo 300 milhas de separação entre pares de regiões
- Replicação automática para alguns serviços
- Recuperação de região priorizada em caso de interrupção
- As atualizações são distribuídas sequencialmente para minimizar o tempo de inatividade
- Link da Web: https://aka.ms/PairedRegions-ptb

Regiões Sobenaras do Azure
- Serviços Governamentais dos EUA: Atende às necessidades de segurança e conformidade das agências federais, governos estaduais e locais dos EUA e seus provedores de soluções.
- Azure Governamental: Instância separada do Azure; Fisicamente isolada de implantações que não sejam do governo dos EUA; Acessível somente a pessoal verificado e autorizado;
- Azure China: A Microsoft é o primeiro provedor estrangeiro de serviços de nuvem pública da China, em conformidade com as regulamentações governamentais;
- Recursos do Azure China: Instância fisicamente separada dos serviços de nuvem do Azure operados pela 21Vianet; Todos os dados permanecem dentro da China para garantir a conformidade;

Recursos do Azure
- Os recursos do Azure são componentes como armazenamento, máquinas virtuais e redes que estão disponíveis para criar soluções de nuvem;
- Máquinas virtuais
- Contas de Armazenamento
- Redes Virtuais
- Serviços de Aplicativos
- Bandos de Dados SQL
- Funções

Grupo de Recursos
- Um grupo de recursos é um contêiner que você usa para gerenciar e agregar recursos em uma única unidade
- Os recursos podem existir em apenas um grupo de recursos
- Os recursos podem existir em diferentes regiões
- Os recursos podem ser movidos para diferentes grupos de recursos
- Os aplicativos podem utilizar vários grupos de recursos

# Assinatura da Azure e Grupos de Gerenciamentos

Assinatura do desenvolvimento
Assinatura do teste
Assinatura da produção

- Uma conta pode ter diversas assinaturas, mas uma assinatura está associada apenas a uma conta
- Uma assinatura do Azure fornece a você acesso autenticado e autorizado às contas do Azure

Assinaturas do Azure
- Limite de Cobrança: gere relatórios de cobrança e faturas separados para cada assinatura
- Limite de controle de acesso: gerenciar e controlar o acesso aos recursos que os usuários podem provisionar com assinaturas específicas

Grupos de Gerenciamentos
- Grupos de gerenciamento > Assinaturas > Grupos de Recursos > Recursos
- Os grupos de gerenciamento podem incluir várias assinaturas do Azure
- As assinaturas herdam as condições aplicadas ao grupo de gerenciamento

