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

# Armazenamento do Azure

Objetivos
- Comparar os serviços de armazenamento do Azure
- Descrever as camadas de armazenamento
- Descrever as opções de redundância
- Descrever as opções de conta de armazenamento e os tipos de armazenamento
- Identificar opções para mover arquivos, incluindo o AzCopy, o Gerenciador de Armazenamento do Azure e a Sincronização de Arquivos do Azure
- Descrever as opções de migração, incluindo as Migrações para Azure e o Azure Data Box.

Contas de Armazenamento (Storage Account)
- Deve ter um globalmente nome exclusivo
- Fornecer acesso à Internet em todo o mundo
- Determinar os serviços de armazenamento e as opções de redundância

Redundância de armazenamento
- LRS (armazenamento com redundância local) > DC individual na região primária > 11 noves
- ZRS (armazenamento com redundância de zona) > Três zonas de disponibilidade na região primária > 12 noves
- GRS (armazenamento com redundância geográfica) > Datacenter único no primário e região secundária > 16 noves
- GZRS (armazenamento com redundância de zona geográfica) > Três zonas de disponibilidade na região primária e um único DC na região secundária > 16 noves
- LRS > ZRS > GRS > GZRS

Redundância e Serviços de Armazenamento
- Blob do Azure: otimizado para o armazenamento de quantidades massivas de dados não estruturados, como texto ou dados binários.
- Disco do Azure: fornece discos para máquinas virtuais, aplicativos e outros serviços acessarem e utilizarem.
- Fila do Azure: serviço de armazenamento de mensagens que fornece armazenamento e recuperação para grandes quantidades de mensagens, cada uma com até 64KB.
- Arquivos do Azure: configura um compartilhamento de arquivos de rede altamente disponível que pode ser utilizado usando o protocolo Bloco de Mensaens do Servidor.
- Tabelas do Azure: fornece uma opção de chave/atributo para o armazenamento de dados estruturados não relacionais com um design sem esquema.

Pontos de extremidade públicos do serviço de armazenamento e Camadas de Acesso
- Serviço de armazenamento / Ponto de extremidade público
- Armazenamento de Blobs: https://<storage-account-name>.blob.core.windows.net
- Data Lake Storage Gen2: https://<storage-account-name>.dfs.core.windows.net
- Arquivos do Azure: https://<storage-account-name>.file.core.windows.net
- Armazenamento de filas: https://<storage-account-name>.queue.core.windows.net
- Armazenamento de Tabelas: https://<storage-account-name>.table.core.windows.net

Camadas de acesso de armazenamento do Azure
- Frequente: otimizada para armazenamento de dados acessados com frequência
- Esporádico: otimizada para armazenamento de dados acessados com pouca frequência e armazenados pelo menos 30 dias
- Frio: otimizado para o armazenamento de dados acessados com pouca frequência e armazenados por pelo menos 90 dias
- Arquivo morto: otimizada para armazenamento de dados acessados raramente e armazenados por pelo menos 180 dias com requisitos de latência flexiveis.

Migrações para o Azure
- Plataforma de migração unificada
- Intervalo de ferramentas integradas e autônomas
- Avaliação e migração

Azure Data Box
- Serviço de migração física (até 80TB de dados)
- Armazenar até 80 terabytes de dados
- Mova os backups de recuperação de desastre para o Azure
- Proteja seus dados em uma caixa robusta durante o trânsito
- Migre dados do Azure para conformidade ou necessidades regulatórias
- Migre dados para o Azure de locais remotos com conectividade limitada ou sem conectividade

Opções de Gerenciamento de Arquivos
> AzCopy
- Utilitário de linha de comando
- Copiar blobs ou arquivos de ou para sua conta de armazenamento
- Sincronização em uma direção

> Gerenciador de Armazenamento do Azure
- Interface gráfica do usuário (de modo semelhante ao Windows Explorer)
- Compatível com Windows, MacOS e Linux

> Sincronização de Arquivos do Azure
- Sincroniza os arquivos do Azure e locais de forma bidirecional
- A camada de nuvem mantém os arquivos acessados com frequência no local, enquanto libera espaço

# Identidade, Acesso e Segurança

ID do Microsoft Entra
- O Microsoft Entra ID é o serviço de gerenciamento de identidades e acesso baseado em nuvem do Microsoft Azure
- Autenticação (os funcionários entram para acessar os recursos)
- Logon único (SSO)
- Gerenciamento de aplicativos
- Negócios para Negócios (B2B)
- Gerenciamento de dispositivos

Microsoft Entra Domain Services
- Obtenha os benefícios dos serviços de domínio baseados em nuvem sem gerenciar os controladores de domínio.
- Execute aplicativos herados (que não podem utilizar os padrões de autenticação modernos) na nuvem.
- Sincronizar automaticamente a partir do Microsoft Entra ID

Comparar a autenticação e a autorização
> Autenticação
- Identifica a pessoa ou serviço buscando acesso a um recurso
- Solicita credenciais de acesso legítimo
- Base para criar princípios de identidade e controle de acesso seguros

> Autorização
- Determina nível de acesso de uma pessoa ou serviço autenticado
- Define quais dados eles podem acessar e o que podem acessar e o que podem fazer com eles

> Autenticação multifator
- Fornece segurança adicional para as identidades exigindo dois ou mais elementos para autenticação completa
- Algo que você sabe > Algo que você possui > Algo que você é

> B2B do Microsoft Entra External ID

> B2C do Identidades Externas do Azure AD

> Acesso Condicional
- Associação de usuário ou grupo
- Local do IP
- Dispositivo
- Aplicativo
- Detecção de risco

Controle de acesso baseado em função
- Gerenciamento de acesso de granularidade finais
- Divida as tarefas dentro da equipe e conceda somente a quantidade de acesso de que os usuários precisam para trabalhar
- Habilite o acesso ao portal do Azure e o controle de acesso aos recursos

Confiança Zero
- Proteja os ativos onde eles estiverem com a Confiança Zero
- Proteção completa (segurança física, Identidade e acesso, Perímetro, Rede, Computação, Aplicativo e Dados)
- Uma abordagem em camadas para proteger sistemas de computador
- Fornece vários níveis de proteção
- Ataques contra uma camada são isolados das camadas subsequentes

Microsoft Defender para Nuvem
- O Microsoft Defender para Nuvem é um serviço de monitoramento que fornece proteção contra ameaças nos datacenters do Azure e locais

==============================================================================================================
# Gerenciamento de Custos na Azure

Gerenciamento de Custos
- Calculadora de custos e preços
- Gerenciamento de custos e marcas

Computação em nuvem: domínio do objetivo
- Descrever fatores que podem afetas os custos no Azure
- Compare a calculadora de preços e a calculadora de custos total de propriedade (TCO)
- Descreva a Ferramenta de Gerenciamento de Custos do Azure
- Descrever a finalidade das marcas

Fatores que afetam os custos
- Este são alguns dos fatores que afetam os custos:
1) Tipo de recurso: os custos são específicos do recurso, portanto, o uso que um medidor rastreia e o número de medidores associados a um recurso, dependendo do tipo de recurso.
2) Consumo: Com um modelo pago conforme o uso, o consumo é um dos maiores geradores de custos.
3) Manutenção: Monitorar seu volume do Azure e manter seu ambiente pode ajudá-lo a identificar e reduzir os custos que não são necessários, como ao desligar máquinas virtuais subutilizadas.
4) Área geográfica: O mesmo tipo de recurso pode custar valores diferentes dependendo da área geográfica, o que afeta os custos do Azure.
5) Tráfego de rede: Embora algumas transferências de dados de entrada sejam gratuitas, o custo para dados de saída ou dados entre recursos do Azure é afetado por zonas de cobrança.
6) Assinatura: O tipo e a configuração da assinatura também podem afetar o custo. Por exemplo, a avaliação gratuita permite explorar alguns recursos do Azure gratuitamente.

Explorar o Azure Marketplace
- O Azure Marketplace permite que os clientes encontrem, experimentem, comprem e provisionem aplicativos e serviços de centenas de provedores de serviços líderes, que são todos certificados para execução no Azure.
- Plataformas de contêiner de software livre
- Imagens da máquina virtual e do banco de dados
- Software de compilação e implantação de aplicativos
- Ferramentas para desenvolvedores
- E muito mais, com mais de 10.000 itens listados!

Calculadora de preços - Calculando o Custo Total no Azure
- A calculadora de preços é uma ferramenta que ajuda a estimar o custo dos produtos do Azure.
- As opções que você pode configurar na calculadora de preços variam entre os produtos, mas as opções básicas de configuração ingcluem
1) Região
2) Camada
3) Opções de cobrança
4) Opções de suporte
5) Programas e ofertas
6) Preço de Desenvolvimento/Teste do Azure

Calculadora de custo total de propriedade (TCO)
- Uma ferramenta para estimar a economia de custos possível ao migrar para o Azure
- Um relatório compara os custos das infraestruturas locais com os custos de uso de produtos e serviços do Azure na nuvem

Gerenciamento de Custos do Azure
- Relatório: relatórios de cobrança
- Enriquecimento de dados
- Orçamentos: definir orçamento de gastos
- Alertas: quanto o custo excede os limites
- Recomendação: recomendações de custo

Marcas
- Fornecem metadados aos recursos do Azure
- Organizam os recursos em uma taxonomia de maneira lógica
- Consistem em um par nome-valor
- Muito úteis para reunir informações de cobrança
