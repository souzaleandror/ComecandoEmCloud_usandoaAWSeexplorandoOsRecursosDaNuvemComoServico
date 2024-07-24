##### 23/07/2024

Curso de Começando em Cloud: usando a AWS e explorando os recursos da nuvem como serviço

@01-Navegando na nuvem

@@01
Apresentação

Olá, meu nome é Lucas Mata e sou instrutor aqui na Alura.
Audiodescrição: Lucas se considerada uma pessoa branca. Usa óculos de armação preta, fina e arredondada e tem cabelo curto e preto. Veste uma camiseta preta com o escrito "Alura". Está no estúdio da Alura; ao fundo, uma parede com iluminação vermelha e azul. À direita, uma estante com decorações e um letreiro do logotipo da Alura.
Boas-vindas ao curso!

O que vamos aprender?
Se você deseja aprender mais sobre computação em nuvem e dar os primeiros passos na Cloud, este curso é ideal para você. Neste curso, abordaremos os seguintes tópicos:

Primeiramente, os fundamentos da computação em nuvem serão explorados. Em seguida, aprenderemos como selecionar serviços na Cloud. Também vamos abordar o gerenciamento de ambientes na AWS, incluindo a criação e gestão de instâncias. Vamos subir um servidor Apache na instância criada com uma aplicação web de teste. Além disso, exploraremos o acesso à AWS através da CLI e conheceremos ferramentas como AWS SDK, CloudWatch e VPC.

Abordagem de aprendizado
Vamos aprender tudo isso de maneira contextualizada, explorando todos esses tópicos através de um projeto prático: uma aplicação web de teste que estará acessível publicamente na internet.

Além dos vídeos, aproveite os recursos adicionais oferecidos na plataforma, como atividades práticas e suporte através do fórum e da comunidade no Discord.

Estamos prontos para mergulhar juntos no mundo da Cloud!

@@02
Identificando a computação como serviço

Precisamos criar um website para hospedar conteúdos sobre tecnologia. Desejamos compartilhar informações e experiências, utilizando softwares e ferramentas de DevOps.
Quando pensamos em um website, temos uma série de dados que são carregados no navegador de uma pessoa usuária. Por exemplo, ao visitar o site da Alura, encontramos as diferentes escolas que compõem a plataforma. Se clicarmos na escola de "Data Science" (Ciência de Dados), receberemos imediatamente uma série de informações: vídeos, imagens e um conteúdo bastante interativo.

Mas essas informações não estão armazenadas no nosso computador. Estamos acessando dados que residem em um computador disponível na web.

Entendendo o servidor
Como escolhemos onde hospedar este website? Esse computador é conhecido como servidor. E ele recebe esse nome por um motivo claro: está constantemente respondendo às solicitações das pessoas usuárias, como quando alguém clica no ícone da escola de Ciência de Dados e obtém todas as informações associadas a ela.

Clientes -> Internet -> Servidor
Esse computador estará constantemente respondendo a essas solicitações e enviando todas as informações necessárias para os dispositivos que conhecemos como clientes, como nossos telefones, notebooks, ou até mesmo a televisão em casa. Assim, de um lado temos o servidor e do outro lado temos os dispositivos clientes.

Localização do servidor
O servidor pode estar localizado em nossa própria casa. Podemos configurar um desktop para ficar ligado 24 horas por dia, 7 dias por semana, atendendo continuamente às solicitações das pessoas. No entanto, existe uma solução possivelmente mais prática que conhecemos como cloud computing (computação em nuvem).

Cloud computing
O conceito de computação em nuvem consiste na oferta de serviços computacionais, como armazenamento e hospedagem de websites, como um serviço para pessoas usuárias através da rede.

Principal vantagem do cloud computing
Não precisamos nos preocupar com um computador pessoal ligado em casa o tempo todo. Não é necessário realizar atualizações constantes nem verificar se ele está conectado e respondendo de forma eficiente às solicitações das pessoas usuárias.

Deixamos todas essas responsabilidades a cargo de um provedor de serviços. Assim, nossa preocupação passa a ser especificamente a aplicação em si, cuidando do conteúdo e garantindo uma experiência mais interativa e significativa para as pessoas usuárias que estão navegando na plataforma.

Não apenas para hospedar websites, podemos utilizar uma solução de computação em nuvem. Utilizamos isso diariamente, por exemplo, ao acessar um serviço de compartilhamento de arquivos através de um drive. Podemos também utilizar serviços de computação em nuvem quando usamos um software através de um navegador.

Isso exemplifica o software as a service (software como serviço). E onde esse software está sendo executado, onde está hospedado? Está em um computador que funciona na nuvem.

Além disso, podemos contar com serviços de armazenamento de bancos de dados na nuvem. Também podemos ter serviços de servidor, os quais usamos para hospedar um website. Portanto, há uma ampla gama de serviços que a computação em nuvem nos proporciona. Sempre considerando que a ideia principal é oferecer recursos computacionais como serviço.

Conclusão e Próximos passos
Já é possível perceber que a melhor opção para hospedar este site é utilizar um serviço de computação em nuvem. Dessa forma, podemos nos concentrar mais no conteúdo do próprio site do que na infraestrutura necessária para sua hospedagem e funcionamento.

Mas onde está localizada exatamente essa "nuvem"? Como as pessoas conseguem acessar o conteúdo que está armazenado em um servidor na nuvem?

@@03
Analisando opções de infraestrutura

Você faz parte da equipe de uma startup que está desenvolvendo uma aplicação web inovadora. Nesse momento, há um debate na equipe sobre como estruturar a aplicação de forma eficiente, garantindo escalabilidade, segurança no armazenamento de informações pessoais de pessoas usuárias e bom desempenho. Sua tarefa é avaliar as opções disponíveis de hospedagem da aplicação para recomendar a melhor abordagem.
Pensando em termos de escalabilidade, segurança e desempenho, o que você recomendaria para sua equipe?

Embora os servidores dedicados ofereçam controle total e possam ser otimizados para desempenho, eles não oferecem a mesma facilidade de escalabilidade e podem
 
Embora os servidores dedicados ofereçam controle total e possam ser otimizados para desempenho, eles não oferecem a mesma facilidade de escalabilidade e podem representar um custo maior e complexidade na manutenção para uma startup em crescimento.
Alternativa correta
Manter a infraestrutura em servidores locais para maximizar a segurança, evitando riscos associados ao uso de cloud computing.
 
Alternativa correta
Utilizar exclusivamente serviços de cloud pública, otimizando a aplicação para funcionar em um ambiente compartilhado com outros usuários (multi-tenant) para reduzir custos.
 
Alternativa correta
Migrar completamente para a cloud, utilizando serviços de cloud computing para todas as operações da aplicação, confiando exclusivamente nos provedores desses serviços.
 
Alternativa correta
Adotar uma abordagem híbrida, combinando servidores locais para dados sensíveis e cloud computing para escalabilidade e flexibilidade.
 
Esta opção equilibra segurança, ao manter dados sensíveis em servidores locais, com a escalabilidade e flexibilidade oferecidas pela cloud computing. Permite à startup escalar recursos conforme a demanda e otimizar custos, alinhando-se às necessidades de uma aplicação web inovadora.

@@04
Para saber mais: funcionalidades comuns da nuvem

A nuvem está cada vez mais presente em nosso cotidiano e muitas vezes sequer percebemos isso. Vamos explorar suas funcionalidades mais comuns?
Armazenamento de dados
Um dos recursos mais populares da nuvem é o armazenamento de dados. Serviços de armazenamento em nuvem são oferecidos por provedores como Google, Microsoft, Amazon e Dropbox, permitindo acessar dados de qualquer dispositivo conectado à Internet. Isso elimina a necessidade de transferências manuais de arquivos e é uma opção confiável para backups e recuperação de dados, garantindo a disponibilidade das informações em caso de falhas.

Muitas aplicações em celulares e notebooks fazem uso desse recurso em suas operações. Anteriormente, os dados eram armazenados localmente em discos rígidos, SSDs e outros dispositivos físicos. Com os avanços tecnológicos, o armazenamento em nuvem se tornou mais popular, permitindo que os usuários armazenem seus dados de forma segura e acessível em servidores remotos.

Compartilhamento de arquivos
Outro recurso bem comum é o compartilhamento de arquivos, a nuvem facilita a colaboração e o compartilhamento de arquivos entre equipes. Ferramentas como Google Docs, Google Drive, Microsoft OneDrive, iCloud e Trello permitem criar, acessar, editar e colaborar em documentos, fotos, planilhas e apresentações, sincronizando e salvando tudo em tempo real na nuvem. Para isso, você só precisa de um dispositivo com conexão à Internet.

Hospedagem de aplicativos
A nuvem também permite a hospedagem de aplicativos, facilitando para pessoas desenvolvedoras e empresas gerenciarem seus aplicativos de maneira escalável e confiável, sem precisar configurar e manter servidores físicos. Amazon Web Services (AWS), Microsoft Azure e Google Cloud Platform possuem vários serviços que podem ser utilizados com essa finalidade.

Processamento de dados
Além de tudo o que já comentamos, a nuvem pode ser usada para processamento de dados, executando tarefas de processamento, análise e armazenamento de grandes volumes de dados.

A flexibilidade e acessibilidade oferecidas pela nuvem são essenciais para indivíduos e empresas modernas, promovendo uma maior colaboração e inovação. À medida que a tecnologia evolui, é provável que vejamos ainda mais recursos e capacidades sendo integrados às soluções em nuvem, solidificando ainda mais sua posição como uma ferramenta indispensável no cotidiano.

@@05
Entendendo onde está a nuvem

Agora que já entendemos o que é a computação em nuvem, a questão que surge é: onde fica a nuvem? Se voltarmos ao site da Alura e clicarmos novamente na escola de Data Science, podemos clicar com o botão direito na página e selecionar a opção "Inspecionar".
No menu exibido à direita, clicamos na opção "Rede" localizada na parte superior direita. Ao interagir com a página da Alura do lado esquerdo e clicar em "Programação", observamos uma série de envios, solicitações e requisições. Isso revela o que realmente está acontecendo na rede. Cada vez que interagimos com o site, fazemos uma solicitação de recursos ao servidor que armazena esse site.

Ao mesmo tempo, ele retorna com o conteúdo da escola de Programação, onde estão todos os principais cursos da escola.

Já deu para entender que a internet é a ligação entre o dispositivo do cliente e o servidor, que pode estar como serviço de computação em nuvem. Ou melhor, são as redes de computadores.

A internet é um sistema global de redes de computadores interligadas.
A seguir, entenderemos como as redes funcionam.

Funcionamento das Redes
Utilizamos um conjunto de protocolos toda vez que interagimos com o site, precisamos nos conectar com um dispositivo, seja para enviar um arquivo ou receber um conjunto de dados.

Protocolos
O que são esses protocolos? Eles nos ajudam a organizar o pedido ou o encaminhamento de dados em pacotes. Esses pacotes recebem o endereço de origem, que é o nosso computador encaminhando a solicitação para o site, e também precisam do endereço de destino, para onde o pacote deve ser enviado.

Por isso, todos os dispositivos conectados à internet recebem um endereço de identificação único, conhecido como endereço IP, que é também o nome do protocolo IP.

Modelo TCP/IP
O IP é a identificação individual de cada um dos dispositivos conectados à internet ou a redes privadas.
O protocolo TCP, que dá nome ao modelo TCP/IP utilizado como base na construção das redes de computadores, é responsável pela conexão entre nosso dispositivo e o servidor de destino, que armazena o site, atuando na camada de transporte.

Esquema do modelo TCP/IP. No topo, há um notebook de onde saem quatro etapas numeradas de 1 a 4, simbolizando partes de um puzzle, que indicam as camadas. As etapas estão conectadas por linhas pontilhadas a um ícone de globo, simbolizando a distribuição pela internet. Abaixo, as mesmas quatro camadas conectam-se a outro notebook, representando o servidor. 

Essa imagem mostra que a requisição e o conjunto de dados passam por várias camadas antes de serem preparados para serem encaminhados através de uma série de dispositivos interconectados.

Isso porque o servidor que armazena esse site pode estar localizado fora da nossa cidade, possivelmente em outro país ou continente, além da área de cobertura do nosso provedor de internet. Para que nossa requisição alcance esse servidor, ela precisa passar por uma série de dispositivos de rede intermediários, como os roteadores, os quais frequentemente reiniciamos em casa quando a conexão está instável, até chegar ao endereço de destino.

Camadas do TCP/IP
Nesse modelo, temos quatro principais camadas.

Camada de aplicação
A primeira é a camada de aplicação, que está próxima ao nosso site. É nessa camada que inspecionamos os pacotes, solicitações e requisições. Um dos principais protocolos que operam nesta camada é o HTTP, e sua versão segura HTTPS.

Camada de transporte
A camada de transporte utiliza o protocolo TCP para garantir a entrega confiável dos pacotes nessa conexão segura.

Camada de rede
Na camada de rede, o principal protocolo é o IP, que realiza o endereçamento dos pacotes, especificando sua origem e destino.

Camada de acesso à rede
A camada de acesso à rede, por sua vez, estabelece a conexão física entre os dispositivos.

Na formação das redes, não são apenas os dispositivos clientes, como nossos computadores ou celulares, que estão envolvidos. Também existem os dispositivos de rede, especializados em conectar diferentes redes ao redor do mundo e entre países, encaminhando pacotes e facilitando essa interconexão.

E onde a nuvem se encaixa nisso tudo?

Localizando a Nuvem
A nuvem é um servidor ou um conjunto de servidores conectados à rede global de computadores, que é a internet.
Quando mencionamos serviços de computação em nuvem, geralmente nos referimos a data centers ("centro de dados"), que são sistemas compostos por múltiplos computadores com grande capacidade de processamento e armazenamento centralizados em um único local.

Esses data centers estão conectados à internet através de redes de alta velocidade, o que permite acessar e armazenar informações rapidamente, além de atender às solicitações rapidamente sempre que clicamos no ícone do site para enviar uma resposta ao nosso dispositivo.

Uma coisa que as pessoas usuárias nunca querem é esperar muito tempo para carregar uma página. Por isso, a conexão é fundamental tanto para a pessoa usuária quanto para os data centers.

Conclusão e Próximos passos
Era inimaginável ter a computação como um serviço usando computação em nuvem cerca de uma década atrás. Por quê? Nossas velocidades de conexão eram bastante baixas, então carregar um vídeo no YouTube, por exemplo, podia levar um tempo considerável. Usar um software como serviço no navegador era pouco prático. Era mais eficiente e rápido ter o software instalado diretamente em nosso desktop.

Usar a computação em nuvem como um serviço é uma excelente solução para nosso site. No entanto, com a enorme quantidade de provedores e serviços disponíveis atualmente, pode ser difícil escolher qual deles utilizar. Como decidir entre tantas opções?

Vamos analisar essa questão a seguir!

@@06
Para saber mais: tipos de Cloud

Atualmente temos três tipos principais de Cloud. Que tal analisarmos cada um deles?
Cloud Pública
É o tipo mais comum de cloud, sendo amplamente utilizado por empresas de vários setores. Nesse tipo, os serviços são mantidos por um provedor, como Google, Microsoft, Amazon, Oracle ou IBM.

Esses provedores possuem data centers com servidores interconectados que compartilham recursos e serviços entre as pessoas usuárias. Trata-se, portanto, de uma solução de cloud bem prática e escalável.

Cloud Privada
Ao contrário da cloud pública, a cloud privada oferece uma infraestrutura dedicada exclusivamente a uma organização. Isso significa mais controle e segurança, já que os recursos não são compartilhados com outras empresas. A nuvem privada pode ser hospedada no data center da própria empresa.

Você sabia que pode construir sua própria nuvem em casa? Um exemplo simples é usar uma Raspberry Pi para criar uma nuvem pessoal. A Raspberry Pi é um microcomputador de baixo custo e alta versatilidade, ideal para projetos de tecnologia. Com isso, você terá uma nuvem privada em casa, garantindo total controle e segurança sobre seus dados, similar ao que uma organização obteria com uma infraestrutura de cloud privada.
Cloud Híbrida
Essa opção combina o melhor dos dois mundos, pública e privada. Por exemplo, você pode usar a nuvem pública para executar sistemas e a privada para armazenar dados sensíveis. É uma solução flexível que permite otimizar recursos e segurança conforme necessário.

Além desses tipos de cloud, você pode se deparar com o termo On Premises. Isso refere-se a quando toda a infraestrutura de TI, como servidores e máquinas, está localizada fisicamente na empresa, na conhecida "sala de servidores" ou CPD (Centro de Processamento de Dados). Enquanto a nuvem oferece flexibilidade e escalabilidade, o ambiente On Premises proporciona controle total sobre a infraestrutura.
Escolher a solução certa depende das suas necessidades específicas de segurança, controle e escalabilidade. Compreender essas opções permite tomar decisões informadas e alinhadas com as necessidades e objetivos da sua organização.

@@07
Criando uma conta na AWS!

Decidimos usar a Computação em Nuvem para hospedagem do nosso site, mas ainda temos uma questão em aberto. Há uma grande variedade de provedores de serviços de Computação em Nuvem.
Serviços oferecidos pelos provedores
Qual deles devemos escolher? Todos esses principais provedores oferecem conjuntos de serviços semelhantes. Eles disponibilizam serviços de infraestrutura, plataforma e aplicação. Por exemplo, aplicação como serviço para hospedar software e plataforma como serviço para hospedar websites.

E infraestrutura como serviço significa descentralizar toda a infraestrutura, como o data center que poderíamos ter localmente na nossa organização, e deixar isso sob os cuidados de um provedor de serviços de Computação em Nuvem.

Dentro dessas três principais classes de serviços de Computação em Nuvem, encontraremos diversas soluções que serão analisadas ao longo do curso. Vamos agora examinar os três principais líderes de mercado:

Google Cloud Platform;
Amazon Web Services (AWS);
Microsoft Azure.
Com os sites dos três abertos no navegador, podemos começar analisando a AWS.

Amazon Web Services
A AWS é uma das principais líderes de mercado em provedores de serviços de Computação em Nuvem, sendo pioneira na oferta desses serviços por volta de 2006, 2007.

Se analisarmos na página da AWS, encontraremos um nível gratuito e uma variedade de soluções para migração e operação de serviços de Computação em Nuvem. A AWS é conhecida por ser um dos players mais famosos, justamente por ter um conjunto diversificado de serviços e uma abrangência global significativa de data centers.

Google Cloud
Se acessarmos o site da Google Cloud, a primeira coisa que encontramos é o foco em inteligência artificial, um campo atualmente em alta. A Google Cloud oferece uma variedade de serviços e soluções para desenvolver algoritmos de IA e disponibilizar essas soluções através da rede.

Microsoft Azure
A Microsoft Azure se destaca especialmente quando precisamos integrar aplicações da própria Microsoft. Ela facilita a integração entre a nuvem e as aplicações que usamos diariamente na organização ou no trabalho.

Opções de pagamento para serviços
É importante considerar o modelo de pagamento ao decidir sobre o serviço. Nenhuma plataforma oferece serviços de Computação gratuitamente. Todas funcionam de maneira semelhante, utilizando o modelo "Pay As You Go", ou seja, pagamento conforme o uso, como é evidenciado na página da Microsoft Azure.

Assim, pagamos apenas pelo que consumimos de fato. Além disso, oferece um período de teste gratuito. Durante esse período, os provedores disponibilizam diversos serviços para teste gratuito, permitindo que nos familiarizemos com a plataforma e avaliemos os diferentes serviços disponíveis.

Avaliação das escolhas disponíveis
Precisamos tomar uma decisão entre os três principais players. Uma boa escolha para hospedar o website é usar os serviços da AWS. Isso porque a AWS oferece o maior conjunto de serviços e é a mais utilizada no mercado atualmente.

Todas essas plataformas oferecem categorias de serviços muito similares. O que geralmente difere entre elas é o nome dos serviços e a maneira como são configurados. No entanto, a essência dos serviços utilizados para hospedar um website, por exemplo, será praticamente a mesma.

Vamos começar criando uma conta na AWS.

Criação de conta na AWS
Acessando a página da AWS, localizamos o botão "Conclua o cadastro" no centro. Podemos clicar na opção logo abaixo "Criar uma nova conta da AWS".

Ao clicarmos nesse botão, uma página será exibida, onde precisaremos inserir o endereço de e-mail do usuário raiz e selecionar um nome da conta da AWS.

Podemos vincular com um e-mail digitando o e-mail no campo correspondente. E posteriormente digitar um nome da conta. No meu caso, vou inserir um nome para esse usuário, como "lucas.mata". Clicamos em "Verificar endereço de e-mail" na parte inferior.

Depois, eles enviarão um código para o e-mail cadastrado e o inseriremos no campo "Código de verificação".

Recebemos o e-mail com o código, copiamos e agora vamos inseri-lo no campo indicado e clicar em "Verificar". Com isso, nosso endereço de e-mail foi verificado.

Agora, precisamos escolher uma senha para nosso usuário. Digitamos a senha no campo "Senha do usuário raiz" e depois confirmamos em "Confirmar senha do usuário raiz". Após inserir a senha desejada, podemos clicar em "Continuar". Assim, concluímos nossa primeira etapa.

A segunda etapa são as informações de contato. Primeiro, indicamos que é para nossa conta pessoal, usada para aprendizado, clicando em "Pessoal - para seus próprios projetos".

Ele nos pedirá o nome completo, número de telefone, código do país, país ou região e endereço. Após preenchermos todos os dados corretamente, podemos clicar em "Continuar".

Chegamos a uma tela onde precisamos inserir as informações de um cartão de crédito. Isso ocorre porque o pagamento dos serviços é baseado no nosso consumo. Eles solicitam algumas informações para verificação, mas só haverá cobrança se excedermos os limites dos serviços durante o período de teste.

Portanto, se já possui uma conta na AWS e está explorando o que vamos ver ao longo do curso, tome cuidado para não ser cobrado inadvertidamente. Sempre que utilizamos um serviço, há a possibilidade de cobrança. Por isso, é crucial usar apenas os serviços disponíveis dentro do período de teste, que oferece uma certa gratuidade.

Algumas plataformas oferecem créditos iniciais, ou seja, concedem um valor em dólares para utilizarmos uma quantidade limitada de serviços, permitindo aprendermos a usar a plataforma e ganhar experiência.

Inserimos os dados do cartão e depois clicamos em "Verificar e continuar" para avançar para a próxima etapa.

Na quarta etapa, eles pedem para confirmarmos nossa identidade. Fazemos isso inserindo o número do telefone celular para receber um SMS ou uma chamada de voz, conforme nossa preferência de acesso. Inserimos as informações do telefone, preenchemos o teste de verificação de segurança e depois clicamos em "Enviar SMS". Ao recebermos o código de quatro dígitos, inserimos o código no campo de "Verificação código" e selecionamos "Continuar".

Conclusão e Próximos passos
Assim, concluímos a criação da nossa conta na AWS. Com a conta criada na AWS, no painel de serviços (console), agora é hora de selecionarmos os serviços e entendermos melhor como proceder nesse processo de seleção.

Vamos lá?

@@08
Faça como eu fiz: criando uma conta na AWS

A Amazon Web Services, mais conhecida como AWS, é uma das maiores e mais populares plataformas de computação em nuvem do mundo. Lançada pela Amazon em 2006, a AWS oferece uma grande variedade de serviços possibilitando que empresas, desenvolvedores e pessoas em geral criem e gerenciem aplicações e infraestrutura na nuvem de modo eficiente e escalável.
A AWS é líder no mercado de computação em nuvem, com uma participação significativa no setor. Ela compete principalmente com outros grandes provedores de cloud como Microsoft Azure, Google Cloud Platform (GCP) e IBM Cloud.

Atualmente, conta com mais de 200 tipos de serviços e 105 regiões de disponibilidade (datacenters) distribuídos em 33 regiões geográficas ao redor do mundo. Há planos de expansão em curso para mais seis regiões e criação de 18 novas regiões de disponibilidade, segundo dados da própria AWS.

Durante a aula, optamos por usar os serviços da AWS para hospedagem da nossa aplicação de teste devido a sua abrangência, liderança no mercado e variedade de serviços. Nosso primeiro passo foi criar uma conta na AWS para avaliar e utilizar os seus serviços.

Que tal criar sua própria conta na AWS? Acesse o site da AWS para iniciar sua jornada de aprendizagem!

Para saber mais detalhes sobre o processo de criação de conta na AWS, clique na opinião da pessoa instrutora!

Vamos criar uma conta na AWS!
Antes de mais nada, use os serviços da AWS com bastante atenção, pois a plataforma opera no modelo de pagamento sob demanda e todos os serviços possuem custos associados.

Quando criamos uma conta, a AWS nos fornece créditos para explorarmos alguns serviços de modo gratuito por algum tempo. É possível aprender bastante sobre os serviços da nuvem usando esses créditos, mas devemos ficar atentos para não ultrapassar o seu uso e receber alguma cobrança inesperada.

Passo 1: Acesse a AWS
Então, vamos dar o primeiro passo acessando o site da AWS. No canto superior direito, você verá um botão chamado "Create an AWS Account". Clique nele para começar.

Passo 2: Preencha o formulário de cadastro
Agora, você vai preencher um formulário com suas informações básicas. Coloque seu endereço de e-mail, escolha uma senha forte e insira o nome da sua conta. Utilize um e-mail que você tenha acesso rápido, pois você vai precisar confirmar algumas nos próximos passos.

Passo 3: Insira mais informações
Depois de preencher esses dados, clique em "Continue". A próxima tela vai pedir mais detalhes, como seu nome, número de telefone e endereço. Preencha tudo com cuidado. Aqui, você também precisará escolher o tipo de conta. Para você, como estudante, uma conta pessoal é a melhor escolha.

Feito isso, clique em "Create Account and Continue"!

Passo 4: Insira os dados de pagamento
Agora, vamos para a parte de pagamento. Não se preocupe, você não será cobrado de imediato, mas a AWS fará uma verificação da existência do cartão informado (geralmente com uma cobrança simbólica de U$ 0,00). Insira os dados do seu cartão de crédito ou débito. AWS usa isso para verificar sua identidade e garantir que você seja uma pessoa real.

Após inserir as informações de pagamento, clique em "Verify and Continue". Você verá uma tela para verificação de identidade. AWS vai enviar um código para o seu celular, então tenha ele por perto. Insira o código quando receber e clique em "Verify Code".

A seguir, você escolherá um plano. Para começar, o plano gratuito é ideal. Ele te dá acesso a muitos serviços sem custo, ótimo para aprender e experimentar. Selecione o plano gratuito e clique em "Complete Sign Up".

Passo 5: Faça o login na sua conta
Pronto! Sua conta na AWS está criada é só fazer o login. Agora, você pode explorar o console da AWS e começar a usar os serviços disponíveis.

Lembre-se de sempre verificar o que está usando para evitar cobranças inesperadas.

@@09
O que aprendemos?

Nessa aula, você aprendeu como:
A computação em nuvem (cloud computing) é usada para operação de aplicações web que fazem parte do nosso cotidiano;
Recursos computacionais estão estruturados como serviços em nuvem para simplificar o atendimento de demandas de software, plataforma e infraestrutura;
Avaliar e selecionar provedores de cloud para implantação de uma aplicação web;
A evolução e difusão da tecnologia de comunicação em redes (internet) possibilitou o desenvolvimento da nuvem para oferta de conjuntos diversificados de serviços;
Criar uma conta na AWS para utilização de serviços de cloud computing.

##### 25/07/2024

@02-Avaliando serviços, segurança e regiões

@@01
Selecionando serviços na Cloud

Agora que já criamos nossa conta na AWS e estamos acessando o console, podemos ver algumas seções principais. Vamos entender quais são elas!
Estrutura do console
Do lado esquerdo, há uma seção com os serviços que visitamos recentemente. Do lado direito, há uma seção para as aplicações que podem estar sendo executadas na nossa conta.

Descendo um pouco mais a página, à direita, encontramos informações sobre custos e os serviços que estamos utilizando no momento. Notem que há um custo associado à conta, por isso é crucial, ao explorar o ambiente em nuvem, ficarmos atentos para desativar qualquer serviço que não esteja mais sendo utilizado, a fim de evitar cobranças desnecessárias.

Navegando pelos serviços
De volta ao topo da página, no canto superior esquerdo da tela, clicando em "Serviços", veremos uma lista variada de serviços. Inicialmente, pode parecer confuso, mas lembrando do nosso objetivo de hospedar um site usando um serviço de computação em nuvem, vamos focar nas cinco principais categorias de serviços aplicáveis a esse problema.

Na parte superior do menu suspenso, clicamos em "Todos os serviços" e em "Visualizar todos o serviços" para visualizar todas as categorias. Vamos começar pela categoria "Computação".

Computação
Como o próprio nome sugere, essa categoria é dedicada à oferta de serviços para execução de aplicações em servidores virtuais. Se estiver acessando a página da AWS em inglês, a categoria aparecerá como "Compute".

Dentro da categoria de computação, temos vários serviços, como EC2, Lambda e Lightsail. O EC2, ou Elastic Compute Cloud, oferece a opção de criar servidores virtuais, conhecidos como instâncias, e será crucial para o nosso projeto.

Instância se refere a uma máquina virtual na infraestrutura de nuvem.
Já o Lambda oferece serviços computacionais do tipo serverless (sem servidor), mas como vamos utilizar um serviço que requer servidores, o EC2 é a escolha ideal.

Armazenamento
Além do serviço de computação, precisaremos de serviços de armazenamento para guardar dados, textos e vídeos do site, similar ao que a plataforma da Alura faz. Um exemplo é o S3 (Simple Storage Service), que é um dos serviços de armazenamento disponíveis.

Banco de dados
Também vamos necessitar de serviços de banco de dados para validar o acesso de clientes a conteúdos exclusivos do site, como áreas que requerem login e senha. Esses bancos de dados são essenciais para gerenciar essas validações.

Redes e entrega de conteúdo
Para armazenar e acessar as aplicações em execução na nuvem, precisaremos de serviços de rede. Esses serviços permitem configurar a rede para melhorar a experiência do usuário e garantir a disponibilidade do conteúdo, por exemplo, replicando o site em múltiplos datacenters dentro de uma região. Isso é feito utilizando serviços de rede e entrega de conteúdo.

Segurança, identidade e conformidade
Por fim, um serviço fundamental é o de segurança, identidade e conformidade, conhecido como IAM. Este serviço gerencia quem pode acessar determinados serviços dentro de uma conta ou organização e define como esse acesso será feito. É um componente crucial para configurar e gerenciar serviços de computação em nuvem.

Próximos passos
Vamos explorar o IAM com mais detalhes a seguir, para entender como configurar o acesso ao servidor e garantir sua segurança.

@@02
Para saber mais: recursos na AWS

Explorar o menu de serviços do console da AWS é encontrar uma lista com uma grande variedade e quantidade de recursos disponíveis. São tantos tipos diferentes que, no começo, podemos até ficar meio confusos com a diversidade de informações.
Vamos detalhar um pouco mais aqui os principais serviços de armazenamento, computação, banco de dados e monitoramento para facilitar sua jornada no mundo da cloud computing (computação em nuvem).

Armazenamento
O Amazon Simple Storage Service (S3) é o principal serviço de armazenamento de dados da AWS. O S3 se destaca pela capacidade de fornecer segurança robusta, escalabilidade flexível e desempenho eficiente.

Com o S3, podemos armazenar e recuperar qualquer quantidade de dados a qualquer momento, de forma segura e acessível. Podemos adotá-lo em diferentes contextos, desde armazenamento de dados para websites e aplicativos móveis até backup e recuperação de desastres.

No S3, o armazenamento de dados trabalha com Objetos e Buckets.

Um objeto é composto por um arquivo e os metadados que descrevem esse arquivo. Já o bucket funciona como um contêiner para esses objetos.

Computação
O Amazon EC2 (Elastic Compute Cloud), é o serviço de computação em nuvem da AWS que permite criar e configurar servidores virtuais de acordo com as suas necessidades específicas.

Com o EC2, você pode selecionar a quantidade de armazenamento, memória, processador e sistema operacional que melhor atendem ao seu projeto.

Vamos imaginar que você está desenvolvendo um aplicativo que precisa processar grandes volumes de dados. Com o EC2, podemos facilmente escalar a capacidade de processamento adicionando ou removendo instâncias de servidores virtuais conforme necessário. Essa característica é muito útil durante picos de uso, como, por exemplo, em lançamentos de produtos ou períodos de promoções especiais (Black Friday, Festas de Fim de Ano, etc).

O Amazon EC2 permite executar diversas instâncias de servidores simultaneamente, garantindo alta disponibilidade e distribuição de carga de trabalho. Ele oferece várias camadas de segurança, incluindo configurações de firewall, permissões de acesso e redes privadas virtuais (VPC), garantindo que nossos dados e aplicações estejam protegidos.

Bancos de dados relacionais
O Amazon RDS (Amazon Relational Databases) é o serviço da AWS que disponibiliza o gerenciamento de base de dados relacionais na plataforma da AWS, focando em escalabilidade e no autogerenciamento. O RDS dá suporte a toda infraestrutura de banco de dados com um conjunto bem resumido de opções no console do RDS.

Por meio dele conseguimos automatizar rotinas de administração de banco de dados, provisionamento de hardware e configurações de backup e restore.

Monitoramento
No Amazon CloudWatch, temos o serviço de monitoramento e observabilidade dos recursos da AWS. Com ele é possível configurar diversas opções de monitoramento e os gastos gerados no consumo de cada recurso.

Esse serviço tem foco especial em pessoas da área de DevOps, em pessoas desenvolvedoras, de engenharia de confiabilidade e de gestão de TI. O CloudWatch entrega uma série de dados e métricas de uso para monitorar as aplicações, a performance e a utilização de todo o sistema.

Entender essas ferramentas é essencial para aproveitar ao máximo o potencial da computação em nuvem e garantir que sua infraestrutura de TI seja eficiente, segura e escalável.

@@03
Elasticidade da nuvem

Imagine que você está trabalhando como pessoa desenvolvedora em uma startup chamada FoodFlow, que oferece um serviço de entrega de alimentos. FoodFlow está prestes a lançar uma grande campanha de marketing e você precisa garantir que a infraestrutura contratada na AWS possa lidar com um aumento repentino no tráfego sem afetar o desempenho do serviço.
Qual abordagem você pode utilizar na nuvem para garantir que a aplicação possa lidar com o aumento de tráfego sem interrupções?

Usar o AWS Lambda para executar todo o código da aplicação, eliminando a necessidade de instâncias EC2 para suportar o pico de acessos.
 
Alternativa correta
Usar o Auto Scaling para adicionar instâncias EC2 automaticamente quando a utilização da CPU ultrapassar um limite específico.
 
Esta abordagem utiliza a elasticidade da nuvem, ajustando dinamicamente os recursos com base na demanda, garantindo eficiência de custo e desempenho durante picos de tráfego.
Alternativa correta
Manter o número atual de instâncias EC2 e aumentar a largura de banda da rede para processar o tráfego adicional.
 
Aumentar apenas a largura de banda não resolve o problema de capacidade computacional necessária para processar o tráfego adicional. A elasticidade da nuvem deve ser utilizada para ajustar os recursos computacionais também.
Alternativa correta
Provisionar um grande número de instâncias EC2 antes da promoção e mantê-las ativas durante o período da campanha.
 
Embora essa abordagem garanta recursos suficientes durante o pico, ela não aproveita a elasticidade da nuvem e resulta em altos custos operacionais quando o tráfego está baixo.
Alternativa correta
Configurar um único servidor de alta capacidade para lidar com todo o tráfego esperado da aplicação durante a campanha.
 
Isso não aproveita a elasticidade da nuvem e representa um único ponto de falha, além de ser menos flexível e potencialmente mais caro.

@@04
Gerenciamento de acesso

A segurança é um aspecto fundamental quando lidamos com aplicações web, como o nosso website. Imagine, por exemplo, que estamos lidando com dados de pacientes em um website de uma clínica médica, onde os bancos de dados contêm resultados de exames clínicos. Esses são dados sensíveis, certo?
Mas quem seria responsável por um eventual vazamento desses dados se estivermos usando um serviço de computação em nuvem? Seríamos nós, a organização que está construindo o website, ou seria o provedor do serviço, como a AWS?

Responsabilidade compartilhada
Quando lidamos com serviços de computação em nuvem, a segurança é uma responsabilidade compartilhada entre o cliente e o provedor de serviços. O provedor, como a AWS, é responsável pela segurança da infraestrutura, da rede e dos servidores físicos que armazenam os dados. Eles garantem, por exemplo, que sempre haverá um backup da aplicação, prevenindo a perda de dados em caso de desastres, como um alagamento no datacenter.

Por outro lado, nós, como clientes, também temos um papel crucial na segurança. Precisamos gerenciar quem pode acessar nossa conta. Para isso, utilizamos o IAM (Gerenciamento de Identidade e Acesso) da AWS.

Implementação da segurança com IAM
No console da AWS, podemos acessar o IAM digitando "IAM" na barra de pesquisa. No painel do IAM, uma das primeiras coisas que pode aparecer é uma notificação informando que a nossa organização não cadastrou um dispositivo de autenticação multifator (MFA). Implementar a MFA é uma boa prática de segurança. Hoje em dia, o vazamento de senhas e nomes de usuários é muito comum. Se nosso usuário e senha vazassem, terceiros poderiam acessar os bancos de dados que criamos e os serviços da AWS que estamos gerenciando.

Portanto, essa recomendação também é uma boa prática que devemos seguir: sempre utilizar autenticação multifator. Mas o que significa multifator? Além da senha, é necessário ter outro mecanismo de identificação para criar duas camadas de segurança antes de permitir o acesso de alguém à conta na AWS.

Gerenciamento de políticas e permissões
No IAM, se olharmos no menu lateral esquerdo, encontramos "Gerenciamento de acesso", que inclui alguns itens como "Grupo de usuários", "Usuários", "Funções" e "Políticas".

O conceito fundamental aqui é o de política. Se clicarmos em "Políticas", encontraremos um objeto da AWS que define permissões específicas. Através das políticas, podemos estabelecer quais são os papéis que cada usuário dentro da organização ou conta pode desempenhar.

Criando uma política
Por exemplo, podemos criar uma política para permitir que um usuário crie serviços comuns. Se escolhermos criar uma política para o serviço EC2, que é a criação de instâncias de computação mencionada anteriormente, podemos definir quais ações são permitidas para essa política. Podemos conceder permissões para criar, excluir ou gerenciar instâncias EC2, entre outras ações disponíveis.

Assim, uma política é essencialmente um conjunto de regras de permissões. Quando criamos uma política, podemos atribuí-la a um usuário específico ou a um grupo de usuários. Isso significa que a política que criamos para o EC2 pode ser atribuída a qualquer usuário ou grupo dentro da nossa organização, concedendo-lhes a capacidade de criar e gerenciar instâncias conforme necessário.

Assim como criamos uma política para o EC2, poderíamos fazer o mesmo para um serviço de banco de dados ou qualquer outro serviço, como, por exemplo, os relacionados a machine learning, que também podem ser utilizados na criação de políticas.

Ao configurar as ações relacionadas ao EC2, podemos definir se essas atribuições serão aplicadas a um recurso específico ou a todos os recursos disponíveis. Vamos aplicar essas ações a todos os recursos e clicar em "Próximo".

Na próxima tela, será solicitado o nome da política. Podemos escolher um nome fácil de lembrar, como "permissao_ec2_org". A descrição é opcional. Vamos simplesmente criar a política.

Atribuindo políticas a grupos e usuários
Observe que a nova política foi criada com sucesso. Uma vez criada, podemos atribuí-la a usuários individuais ou a grupos. É uma prática recomendada atribuir políticas a grupos de usuários, como, por exemplo, Engenharia de Dados ou Machine Learning Engineering, em vez de individualmente. Criar grupos facilita a gestão de permissões conforme as funções dentro da organização, como desenvolvimento ou operações.

Vamos criar um novo grupo para nossa organização clicando em "Criar grupo" no canto superior direito. Vamos nomeá-lo como "devops" e adicionar membros relevantes.

Ao criar o grupo, podemos associar políticas de permissão. Vamos procurar e adicionar a política "permissao_ec2_org" que criamos anteriormente.

Além das políticas que criamos, a AWS também oferece políticas padrão para acesso aos serviços, como "AdministratorAccess". Vamos incluir essa política também para nosso grupo.

Criamos o grupo e atribuímos a ele duas políticas de permissão: a política que criamos e uma política padrão da própria AWS. Isso simplifica nosso trabalho, pois não precisamos criar políticas para serviços que já possuem funções previsíveis e definidas.

Conclusão e próximos passos
Para entender melhor o fluxo de permissões e gerenciamento de acesso, precisamos definir políticas, que são as permissões que usuários ou grupos de usuários possuem dentro da nossa organização. Essas políticas determinam quais serviços um usuário pode acessar na AWS.

Toda vez que um usuário faz login na AWS, o sistema verifica se ele tem autorização para realizar ações como criar ou excluir uma instância, criar um banco de dados, ou visualizar informações armazenadas. Por isso, o gerenciamento dessas permissões é crucial. Ele nos permite, por exemplo, restringir o acesso a dados sensíveis dos nossos clientes, como no caso da clínica médica mencionado anteriormente.

Agora que entendemos melhor o modelo de segurança na nuvem, é hora de avançar. A seguir, vamos explorar a distribuição dos datacenters e como escolhê-los no contexto do nosso website.

@@05
Avaliando estratégias de IAM

Uma startup de tecnologia aplicada à saúde está crescendo rapidamente, e a necessidade de uma estrutura de IAM robusta e segura nunca foi tão crítica. Você, como pessoa do time responsável pela segurança da informação, está avaliando as práticas atuais de IAM na AWS para garantir que os princípios de menor privilégio sejam aplicados. Um dos requisitos definidos pela equipe é a manutenção da flexibilidade do ambiente para o rápido desenvolvimento de produtos.
Neste contexto, o que fazer para melhorar a segurança e a eficiência do gerenciamento de acesso na sua organização?

Implementar políticas de IAM genéricas que concedam acesso amplo aos recursos da AWS para todos os usuários, facilitando o desenvolvimento rápido.
 
Isso contradiz as boas práticas de segurança, especialmente o princípio de menor privilégio, que recomenda conceder apenas as permissões necessárias para realizar uma tarefa.
Alternativa correta
Evitar o uso de grupos de usuários IAM e políticas para manter a flexibilidade do ambiente e configurar o acesso em cada serviço utilizado na AWS.
 
Configurar o acesso diretamente em cada serviço pode levar a inconsistências e dificultar a gestão de permissões, além de não seguir o princípio de menor privilégio e as boas práticas recomendadas para o gerenciamento de acesso.
Alternativa correta
Não estabelecer restrições no IAM e confiar na segurança pela confidencialidade do sistema, assumindo que a AWS provisiona a proteção da infraestrutura.
 
A segurança por obscuridade (confidencialidade do sistema) não é uma prática recomendada, pois não oferece proteção real contra ameaças. É importante implementar controles de acesso robustos e seguir as boas práticas de IAM.
Alternativa correta
Criar um único usuário IAM com privilégios administrativos e compartilhar as credenciais com todos os membros da equipe de desenvolvimento.
 
Compartilhar credenciais de um único usuário IAM é uma prática de segurança ruim, pois dificulta o rastreamento de atividades e aumenta o risco de comprometimento de segurança.
Alternativa correta
Utilizar grupos de usuários IAM para organizar o acesso com base nas funções da equipe, aplicando políticas específicas a cada grupo.
 
Ao criar grupos de usuários baseados nas funções da equipe, você pode aplicar políticas de acesso específicas a cada grupo, garantindo que cada pessoa tenha apenas os privilégios necessários para desempenhar suas atividades. Isso segue o princípio de menor privilégio, mantendo a flexibilidade do ambiente para o rápido desenvolvimento de produtos, conforme o requisito da equipe. Dessa forma, você consegue equilibrar a segurança e a eficiência do IAM na sua organização.

@@06
Distribuindo aplicações em regiões

Agora que entendemos mais sobre segurança e como gerenciamos as identidades e os acessos aos serviços dentro da nossa conta na AWS, é hora de pensar em como vamos hospedar nossa aplicação.
Hospedagem de aplicações web
Sabemos que um website não simplesmente "existe" online. Na verdade, ele está hospedado em servidores físicos interconectados em uma rede. Esses servidores estão localizados em datacenters que possuem capacidades enormes de processamento e armazenamento de dados, todos acessíveis através da rede.

Quando acessamos um site, estamos enviando uma requisição HTTP para o servidor. O servidor, por sua vez, responde enviando todos os dados solicitados que serão carregados em nosso navegador, proporcionando a experiência visual que vemos em plataformas como a Alura.

Latência
Durante esse processo de envio e resposta de requisições, há uma variável crucial chamada latência. A latência mede o tempo que leva desde o envio da requisição até que recebamos a resposta no navegador. Quanto maior a latência, maior o tempo de espera percebido pela pessoa usuária, pois ela aguarda os dados solicitados chegarem do outro lado.

Ela é importante ao criar um website porque influencia diretamente na experiência do usuário. Ninguém quer esperar um ou dois minutos para que a informação solicitada seja carregada no navegador. É fundamental minimizar a latência para proporcionar uma experiência rápida e fluida aos visitantes do site.

Regiões de disponibilidade da AWS
Ao acessarmos o console da AWS, podemos observar que ao lado do nome do nosso usuário, no canto superior direito, está indicado "Ohio", um estado dos Estados Unidos. Se clicarmos nessa opção, encontramos diferentes regiões ao redor do mundo. Essas são as regiões de disponibilidade da AWS, onde estão localizados seus datacenters.

Latência e custo
Ao escolher qual dessas regiões irá hospedar nossa aplicação, precisamos considerar dois aspectos cruciais. O primeiro deles, é a latência. Se optarmos por um servidor que está distante dos locais onde nossos usuários estão localizados, é provável que o tempo de resposta seja maior. Mesmo que a conexão entre os datacenters seja excelente e utilize fibra ótica, os usuários podem perceber essa diferença. A boa prática é sempre hospedar o website o mais próximo possível dos usuários finais da aplicação.

Outro aspecto a considerar é o custo. Lembre-se de que o pagamento é baseado na demanda e os custos de hospedagem podem variar entre as regiões. Por exemplo, se consultarmos a tabela de preços sob demanda da Amazon EC2 para diferentes regiões, veremos que os custos podem variar significativamente.

No caso da América do Sul, como em São Paulo, os primeiros 10 terabytes de transferência de dados para EC2 custam quinze centavos de dólar por gigabyte. Já em Ohio, nos Estados Unidos, esse custo pode ser reduzido para nove centavos por gigabyte transferido. Portanto, o custo também é uma consideração importante ao escolher a região para hospedagem do website. Nem sempre a opção mais próxima geograficamente será a mais econômica.

Zonas de disponibilidade
Dentro de cada uma dessas regiões, há o conceito de "availability zones" (zonas de disponibilidade). Cada zona de disponibilidade funciona como um datacenter independente dentro da mesma região. Temos várias zonas de disponibilidade em uma mesma região para garantir que, se um datacenter em uma zona específica ficar inacessível devido a problemas de rede ou internet, a aplicação ainda permanecerá disponível. É uma forma de assegurar redundância para a aplicação, mesmo que ela esteja hospedada apenas em uma região.

Caso de sucesso: Netflix
A Netflix, um caso de sucesso no entretenimento sob demanda, optou por usar uma infraestrutura em nuvem para facilitar sua operação. Isso significa que eles não precisam manter centros de dados em todas as regiões do mundo nem gerenciar toda essa infraestrutura localmente. Em vez disso, eles delegam essas responsabilidades para provedores como a AWS, garantindo que o conteúdo da Netflix esteja mais próximo dos seus usuários.

Se a Netflix centralizasse todos os seus servidores em uma única região, usuários em diferentes países teriam uma experiência mais lenta, especialmente ao assistir vídeos, que exigem uma transferência de dados maior. Por isso a computação em nuvem se encaixou perfeitamente.

Também é comum que eles distribuam seus serviços em várias regiões ao redor do mundo, considerando que têm usuários globais. Quanto mais próximo fisicamente os dados estão dos usuários, melhor é a qualidade do serviço oferecido.

Hospedagem de websites simples
No caso de um website simples, geralmente escolhemos uma única região para hospedagem, com pelo menos uma zona de disponibilidade para garantir um backup e manter o site sempre disponível, sem interrupções. Isso é crucial, especialmente para sites de e-commerce, onde cada minuto de inatividade significa potencial prejuízo. Erros como 502 ou 504, que indicam problemas do servidor, podem levar os clientes a buscar outras opções para suas compras.

Benefícios da computação em nuvem
A garantia de backup e disponibilidade contínua é um dos principais benefícios da computação em nuvem em comparação com uma infraestrutura local, conhecida como on-premises. Em uma infraestrutura local, se a conexão com nosso escritório ou datacenter local falhar, a aplicação fica inacessível.

Ao optar por um serviço de computação em nuvem que inclui backup e várias zonas de disponibilidade dentro de uma região, garantimos que nossa aplicação funcione sem problemas. Isso não apenas assegura a disponibilidade contínua, mas também proporciona acesso rápido e de qualidade aos usuários, com baixa latência.

Conclusão e próximos passos
No console da AWS, vamos manter a seleção da região de Ohio para executar nossos serviços. Além disso, devemos observar que algumas regiões podem implicar custos adicionais, mesmo durante o período de gratuidade, então é importante verificar a cobertura dos serviços gratuitos em cada região.

Agora que entendemos melhor os conceitos de região, zona de disponibilidade e segurança, criaremos uma instância EC2 para hospedar nossa aplicação web. Vamos nessa?

@@07
Para saber mais: data centers da AWS

Na AWS, podemos escolher a região onde vamos utilizar um determinado serviço. Essa escolha deve ser realizada com cuidado, pois a localização dos data centers pode impactar diretamente no tempo de resposta de uma aplicação devido a latência.
A proximidade geográfica entre os usuários e os servidores pode reduzir a latência e melhorar o desempenho da aplicação. Além disso, a escolha da região pode influenciar fatores como conformidade com regulamentações locais, custos de operação e disponibilidade de serviços específicos.

Para sermos capazes de fazer uma boa escolha, que tal compreendermos melhor como os data centers da AWS estão organizados em regiões (regions), zonas de disponibilidade (availability zones) e zonas locais (local zones)?

Regiões
As regiões são locais físicos ao redor do mundo onde os data centers da AWS estão agrupados. Cada região é constituída por várias zonas de disponibilidade isoladas, fisicamente localizadas em uma determinada área geográfica.

Neste modelo de organização, as zonas de disponibilidade de cada região possuem energia, refrigeração e segurança implementadas de forma independente e se conectam por uma infraestrutura de rede redundante.

Zonas de disponibilidades
As zonas de disponibilidade, ou AZs (availability zones), são conjuntos de data centers operando de forma independente dentro de uma região da AWS. Elas fornecem capacidade de operação de aplicativos, bancos de dados com alta disponibilidade, escalabilidade de infraestrutura e tolerância a falhas.

Toda a infraestrutura das AZs opera sob uma rede de banda larga com fibra dedicada, e toda a comunicação dentro da zona é criptografada.

Zonas locais
As zonas locais visam criar uma proximidade ainda maior para computação, armazenamento, banco de dados e outros serviços AWS. Elas permitem a execução de aplicações que exigem latências de milissegundos para usuários finais, como aplicações de conteúdo multimídia, jogos em tempo real, automação e machine learning.

A escolha correta da região, zona de disponibilidade e zona local é crucial para garantir o desempenho, a segurança e a conformidade da sua aplicação na AWS. Compreendendo tudo isso, você poderá tomar decisões informadas que podem impactar diretamente a eficiência operacional, os custos e a experiência do usuário final.

@@08
Faça como eu fiz: boas práticas de segurança na nuvem

O AWS Identity and Access Management (IAM) é um serviço fundamental na AWS que permite gerenciar o acesso dos usuários aos recursos da nuvem de forma segura.
Com o IAM, é possível criar e gerenciar usuários, grupos e permissões de forma granular, controlando quem pode acessar quais recursos e quais ações podem realizar. Ao criar políticas de acesso, os administradores podem definir permissões específicas para cada usuário ou grupo, limitando o acesso apenas ao necessário para realizar suas tarefas.

Uma das boas práticas fortemente recomendadas no gerenciamento de acesso é o princípio do menor privilégio que consiste em conceder apenas as permissões mínimas necessárias para cada usuário ou grupo, e revisar regularmente as permissões para garantir que estejam alinhadas com as necessidades do negócio e as políticas de segurança.

Que tal praticar as boas práticas de segurança no ambiente de nuvem de uma organização criando grupos de usuários, estabelecendo políticas e permissões aos grupos criados na AWS?

Para mais detalhes sobre o passo a passo desse processo, clique na opinião da pessoa instrutora!

Criando grupos de usuários
Para começar, acesse o console da AWS usando suas credenciais de administrador. Dentro do console, navegue até o serviço IAM. Lá, você encontrará a opção de criar grupos de usuários. Clique em "Grupos" no painel de navegação à esquerda e, em seguida, clique em "Criar grupo".

Siga as instruções para dar um nome ao grupo e, opcionalmente, adicione uma descrição. Após a criação do grupo, você poderá adicionar usuários a ele, selecionando os usuários existentes na sua conta.

Estabelecendo políticas de acesso
Agora que os grupos estão criados, é hora de estabelecer políticas de acesso. Na página de detalhes do grupo que você acabou de criar, clique na aba "Políticas de grupo" e depois em "Anexar políticas". Aqui, você pode escolher entre políticas predefinidas fornecidas pela AWS ou criar suas próprias políticas personalizadas.

Selecione as políticas que se adequam às necessidades do grupo e confirme a sua escolha.

Concedendo permissões
Para estabelecer permissões aos grupos, você precisará associar usuários aos grupos e definir permissões específicas para cada grupo.

Para isso, navegue até a página de detalhes do grupo e clicando na aba "Usuários" para adicionar ou remover usuários do grupo. Uma vez que os usuários estejam no grupo, eles herdarão as permissões associadas a ele através das políticas que você definiu anteriormente.

Lembre-se de revisar regularmente suas políticas de acesso e permissões para garantir que estejam alinhadas com as necessidades do seu negócio e as melhores práticas de segurança da AWS. Se precisar de mais orientações, consulte a documentação oficial da AWS.

@@09
O que aprendemos?

Nessa aula, você aprendeu como:
Diferenciar os principais tipos de serviços de computação em nuvem para selecionar a opção mais adequada em diferentes casos de uso;
Gerenciar o acesso de pessoas usuárias no ambiente de computação em nuvem de uma organização para garantir a segurança das aplicações e dados em nuvem;
Os data centers da AWS estão organizados ao redor do mundo para armazenamento e processamento eficiente de dados e aplicações;
O modelo de responsabilidade compartilhada estabelece as atribuições de segurança dos provedores e das pessoas usuárias para assegurar a proteção dos dados e aplicações em nuvem;
Selecionar região e zonas de disponibilidade para serviços de computação na AWS.