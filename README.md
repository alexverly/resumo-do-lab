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

# Arquiteturas e Serviços no Azure

Computação e rede
- Tipos de Computação
- Hospedagem de aplicativos
- Redes Virtuais

Computação e Rede
- Comparar tipos de computação, incluindo instâncias de contêiner, máquinas virtuais e funções
- Descrever os recursos exigidos para as máquinas virtuais
- Definir pontos de extremidade públicos e privados
- Descrever as opções de máquina virtual, incluindo VMs (máquinas virtuais), conjuntos de dimensionamento de máquinas virtuais, conjuntos de disponibilidade de máquinas virtuais e a área de Trabalho Virutal do Azure.

Serviços de computação do Azure
- A computação do Azure é um serviço sob demanda que fornece recursos de computação, como discos, processadores, memória, rede e sistemas operacionais.

Máquinas Virtuais do Azure
- As máquinas virtuais do Azure (VMs) são emulações de software de computadores físicos
- Inclui processado virtual, memória, armazenamento e rede
- Ofera de IaaS que oferece personalização e controle total
- VMs e contêineres são isolados do hardware do host

Conjuntos de dimensionamento de VMs
- Os conjuntos de dimensionamento oferecem uma oportunidade de balanceamento de carga para dimensionar os recursos automaticamente.

Conjuntos de disponibilidade de VMs
- Domínio de Falha x Domínio de Atualização

Área de Trabalho Virtual do Azure
- A Área de Trabalho Virtual do Azure é uma virtualização da área de trabalho e aplicativo executada na nuvem
- Crie um ambiente completo de virtualização da área de trabalho sem precisar executar outros servidores de gateway.
- Reduza o risco de que o recurso seja deixado para trás
- Implantações reais de várias sessões

Serviços de Contêineres do Azure
- Os contêineres do Azure fornecem um ambiente leve e virtualizado que não exige o gerenciamento do sistema operacional e pode responder a alterações sob demanda.
- Instâncias de Contêiner do Azure: uma oferta de PaaS que executa um contêiner ou pod de contêineres no Azure
- Aplicativos de Contêiner do Azure: uma oferta de PaaS, como instâncias de contêineres, que pode balancear a carga e escala
- Serviço de Kubernetes do Azure: um serviço de orquestração para contêineres com arquiteturas distribuídas e grandes volumes de contêineres

Azure Functions
- É uma oferta de PaaS que dá suporte a operações de computação sem servidor.
- O código baseado em eventos é executado quando chamado, sem exigir uma infraestrutura de servidor durante períodos inativos.

Comparar opções de computação de Azure
> Máquinas virtuais
- Servidor baseado em nuvem que dá suporte a ambientes Windows ou Linux
- Útil para migrações de lift-and-shift para a nuvem
- Pacote do sitema operacional completo, incluindo o sistema operacional do host

> Área de Trabalho Virtual
- Fornece uma experiência de área de trabalho do Windows baseada em nuvem
- Aplicativos dedicados para conexão e uso ou acessíveis de qualquer navegador moderno
- O logon de vários clientes permite que vários usuários façam logon no mesmo computador ao mesmo tempo

> Contêineres (lembre-se do AKS)
- Ambiente leve e em miniatura adequado para execução de microsserviços
- Projetado para escalabilidade e resiliência por meio da orquestração
- Os aplicativos e serviços são empacotados em um contêiner que fica na parte superior do sistema operacional do host. Vários contêineres podem ficar em um sistema operacional do host.

Serviços de Aplicativo do Azure
- Os serviços de Aplicativos do Azure consistem em uma plataforma totalmente gerenciada para criar, implantar e dimensionar aplicativos Web e APIs rapidamente.
- Trabalha com .NET, .NET Core, Node.js, Java, Python ou PHP
- Oferta de PaaS com requisitos de nível corporativo de desempenho, segurança e conformidade

Serviços de rede do Azure
- A Rede Virtual do Azure (VNet) permite que os recursos do Azure se comuniquem uns com os outros, com a Internet e com redes locais.
- Pontos de extremidade públicos, acessíveis de qualquer lugar na Internet.
- Pontos de extremidade privados, acessíveis somente de dentro da sua rede.
- As sub-redes virtuais segmentam sua rede para atender às suas necessidades.
- O emparelhamento de rede conecta suas redes privadas diretamente.

Serviços de rede do Azure: Gateway de VPN
- O gateway é VPN é usado para enviar tráfego criptografado entre uma rede virtual do Azure e uma no local pela Internet pública
- ExpressRoute: estende as redes locais para o Azure por meio de uma conexão privada facilitada por um provedor de conectividade.

DNS do Azure
- Confiabilidade e desempenho aproveitando uma rede global de servidores de nome DNS usando a rede Anycast.
- A segurança do DNS do Azure baseia-se no gerenciador de recursos do Azure, habilitando o controle de acesso baseado em função e o monitoramento e o registro em log.
- Facilidade de uso para gerenciar seus recursos externos e do Azure com um único serviço DNS
- As redes virtuais personalizáveis permitem que você use nomes de domínio provados e totalmente personalizados em suas redes virtuais privadas
- Os registros de alias dão suporte a conjuntos de registros de alias para apontar diretamente para um recurso do Azure
