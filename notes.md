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