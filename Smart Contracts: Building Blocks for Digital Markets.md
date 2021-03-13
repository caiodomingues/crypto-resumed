| | | 
|-|-|
Author | Nick Szabo © 1996 |
Title | Smart Contracts: Building Blocks for Digital Markets |
URL | https://www.fon.hum.uva.nl/rob/Courses/InformationInSpeech/CDROM/Literature/LOTwinterschool2006/szabo.best.vwh.net/smart_contracts_2.html |

Permissão para redistribuir sem alteração.

# Contratos Inteligentes: Blocos de Construção para Mercados Digitais

[Glossário (do documento original)](https://www.fon.hum.uva.nl/rob/Courses/InformationInSpeech/CDROM/Literature/LOTwinterschool2006/szabo.best.vwh.net/smart_contracts_glossary.html)

(Essa é uma reescrita parcial do artigo que apareceu no Extropy #16)

## Introdução

O contrato é um conjunto de promessas acertadas num "encontro de ideias", é a forma tradicional de formalizar uma relação. Embora os contratos sejam usados principalmente em relações comerciais (o foco deste artigo), eles também podem envolver relacionamentos pessoais, como casamentos. Os contratos também são importantes na política, não apenas por causa das teorias do "contrato social", mas também porque a execução de contratos tem sido tradicionalmente considerada uma função básica dos governos capitalistas.

Seja executado por um governo ou de outra forma, o contrato é o alicerce básico de uma economia de mercado livre. Ao longo de muitos séculos de evolução cultural emergiu o conceito de contrato e os princípios relacionados a ele, codificados na lei comum. A [teoria da informação algorítmica](https://www.fon.hum.uva.nl/rob/Courses/InformationInSpeech/CDROM/Literature/LOTwinterschool2006/szabo.best.vwh.net/kolmogorov.html) sugere que essas estruturas evoluídas costumam ser proibitivamente caras para recomputar. Se começarmos do zero, usando a razão e a experiência, podem levar muitos séculos para desenvolver ideias sofisticadas, como os direitos de propriedade, que fazem o mercado livre moderno funcionar [Hayek].

O sucesso da lei comum dos contratos, combinado com o alto custo de sua substituição, faz com que valha a pena preservar e fazer uso desses princípios quando apropriado. No entanto, a revolução digital está mudando radicalmente os tipos de relacionamento que podemos ter. Que partes de nossa tradição jurídica duramente conquistada ainda serão valiosas na era do ciberespaço? Qual é a melhor maneira de aplicar esses princípios de lei comum ao projeto de nossos relacionamentos on-line?

Os computadores possibilitam a execução de algoritmos até então proibitivamente caros e as redes a transmissão mais rápida de mensagens maiores e mais sofisticadas. Além disso, cientistas da computação e criptógrafos descobriram recentemente muitos algoritmos novos e bastante interessantes. A combinação dessas mensagens e algoritmos torna possível uma ampla variedade de novos protocolos.

Novas instituições e novas formas de formalizar as relações que as constituem, agora são possibilitadas pela revolução digital. Eu chamo esses novos contratos de "inteligentes", porque eles são muito mais funcionais do que seus ancestrais inanimados baseados em papel. Nenhum uso de inteligência artificial está implícito. Um contrato inteligente é um conjunto de promessas, especificadas em formato digital, incluindo protocolos nos quais as partes cumprem essas promessas.

## Contratos incorporados ao mundo

A ideia básica dos contratos inteligentes é que muitos tipos de cláusulas contratuais (como ônus, fiança, delineamento de direitos de propriedade, etc.) podem ser incorporados ao hardware e software com os quais lidamos, de forma a violar o contrato caro (se desejado, às vezes proibitivamente) para o invasor. Um exemplo canônico da vida real, que podemos considerar o ancestral primitivo dos contratos inteligentes, é a humilde máquina de venda automática. Dentro de uma quantidade limitada de perda potencial (a quantidade na caixa deve ser menor do que o custo de violação do mecanismo), a máquina recebe moedas e, por meio de um mecanismo simples, que cria um problema de nível de iniciante no projeto com autômatos finitos, dispensa mudar e produzir de forma justa. Os contratos inteligentes vão além da máquina de vendas ao propor a incorporação de contratos em todos os tipos de propriedades valiosas e controladas por meios digitais. Os contratos inteligentes fazem referência a essa propriedade de forma dinâmica e proativa, e fornecem uma observação e verificação muito melhores onde as medidas pró-ativas devem ser insuficientes. E onde a máquina de vendas, como o correio eletrônico, implementa um protocolo assíncrono entre a empresa de vendas e o cliente, alguns contratos inteligentes envolvem várias etapas síncronas entre duas ou mais partes.

Outros precursores de contratos inteligentes incluem terminais e cartões PoS (Ponto de Venda), EDI (Intercâmbio Eletrônico de Dados, usado para pedidos e outras transações entre grandes corporações), e as redes SWIFT, ACH e FedWire para transferência e compensação de pagamentos entre bancos. Estes implementam modelos de segurança comercial, mas muitas vezes com pouca atenção para as necessidades e obrigações contratuais das partes.

## Ataques contra Smart Contracts

Uma declaração ampla da ideia-chave dos contratos inteligentes, então, é dizer que os contratos devem ser *incorporados ao mundo*. Os mecanismos do mundo devem ser estruturados de forma a fazer os contratos.

(a) robusto contra vandalismo ingênuo, e

(b) robusto contra violação sofisticada, compatível com incentivos (racional)

Um vândalo pode ser uma estratégia ou subestratégia de um jogo cuja utilidade é, pelo menos parcialmente, uma função da própria utilidade negativa; ou pode ser um erro de uma parte contratante no mesmo sentido. "Ingênuo" simplesmente se refere à falta de premeditação quanto às consequências de uma violação, bem como à quantidade relativamente baixa de recursos gastos para possibilitar essa violação. O vandalismo ingênuo é comum o suficiente para ser levado em consideração. Uma terceira categoria, (c) vandalismo sofisticado (onde os vândalos podem e estão dispostos a sacrificar recursos substanciais), por exemplo, um ataque militar por terceiros, é de um tipo especial e difícil que muitas vezes não surge em contratos típicos, então que podemos colocá-lo em uma categoria separada e ignorá-lo aqui. A distinção entre estratégias ingênuas e sofisticadas foi formalizada computacionalmente na [teoria da informação algorítmica](https://www.fon.hum.uva.nl/rob/Courses/InformationInSpeech/CDROM/Literature/LOTwinterschool2006/szabo.best.vwh.net/kolmogorov.html).

## Alguns princípios básicos de Contract Design

A ameaça de força física é uma maneira óbvia de inserir um contrato no mundo - fazer com que um sistema judicial decida quais medidas físicas devem ser tomadas por uma agência de execução (incluindo prisão, confisco de propriedade, etc.) em resposta a um quebra de contrato. É o que chamo de forma *reativa* de segurança. A necessidade de invocar a segurança *reativa* pode ser minimizada, mas não eliminada, tornando os arranjos contratuais *verificáveis*, por exemplo, gravando uma violação em uma câmera
de vídeo ou assinando um contrato, a fim de provar reivindicações de violação em tribunal. A *observação* de um contrato em curso, de forma a detectar o primeiro sinal de violação e minimizar as perdas, também é uma forma reativa de segurança. Uma forma *proativa* de segurança é um mecanismo físico que torna a violação cara, como uma fechadura de combinação que torna caro o acesso a uma sala contendo segredos comerciais sem autorização explícita.

Da lei comum, teoria econômica e condições contratuais freqüentemente encontradas na prática, podemos destilar quatro objetivos básicos do desenho do contrato. A primeira delas é a *observabilidade*, a capacidade dos principais de observar o desempenho uns dos outros no contrato, ou de provar seu desempenho para outros principais. O campo da contabilidade está, grosso modo, preocupado principalmente em fazer contratos nos quais uma organização está envolvida mais observáveis.

Um segundo objetivo de *verificabilidade*, a capacidade do principal de provar a um árbitro que um contrato foi executado ou violado, ou a capacidade do árbitro de descobrir isso por outros meios. As disciplinas de auditoria e investigação correspondem aproximadamente à verificação do desempenho do contrato. A observabilidade e a verificabilidade também podem incluir a capacidade de diferenciar entre violações intencionais do contrato e erros de boa fé.

Um terceiro objetivo da concepção do contrato é a *privacidade*, o princípio de que o conhecimento e o controle sobre o conteúdo e a execução de um contrato devem ser distribuídos entre as partes apenas na medida necessária para a execução desse contrato. Esta é uma generalização do princípio da common law da privacidade contratual, que afirma que terceiros, exceto os árbitros e intermediários designados, não devem ter voz na execução de um contrato. A privacidade generalizada vai além disso para formalizar
a afirmação comum: "não é da sua conta". Os ataques contra a privacidade são resumidos por terceiros - Eve, a bisbilhoteira, um observador passivo de conteúdos ou desempenho, e Mallet malicioso, que interfere ativamente no desempenho ou rouba o serviço. Nesse modelo, a privacidade e a confidencialidade, ou seja, a proteção do valor das informações sobre um contrato, suas partes e seu desempenho por parte de Eva, estão incluídas na privacidade, assim como os direitos de propriedade. O campo da segurança
(especialmente, para contratos inteligentes, segurança de computador e rede), corresponde aproximadamente ao objetivo da privacidade.

Um quarto objetivo é a *executoriedade* e, ao mesmo tempo, minimizar a necessidade de execução. Freqüentemente, a capacidade de verificação aprimorada também ajuda a cumprir esse quarto objetivo. Reputação, incentivos embutidos, protocolos de "auto-aplicação" e verificabilidade podem todos desempenhar um papel importante no cumprimento do quarto objetivo. A segurança do computador e da rede também pode contribuir muito para tornar os contratos inteligentes auto-aplicáveis.

Contratos inteligentes geralmente envolvem terceiros de confiança, exemplificados por um intermediário, que está envolvido na execução, e um árbitro, que é chamado para resolver disputas decorrentes da execução (ou falta dela). A privacidade implica que queremos minimizar a vulnerabilidade a terceiros. A verificabilidade e a observabilidade geralmente exigem que os invoquemos. Um mediador deve ser confiável para alguns dos conteúdos e / ou execução do contrato. Um árbitro deve ser confiável para alguns dos conteúdos e um pouco do histórico de desempenho, para resolver disputas e invocar penalidades de forma justa. No projeto de contrato inteligente, queremos obter o máximo dos intermediários e árbitros, ao mesmo tempo que minimizamos a exposição a eles. Um resultado comum é que a confidencialidade é violada apenas em caso de disputa.

No futuro, a distribuição do tamanho das empresas multinacionais se aproximará dos negócios locais, dando origem aos [pequenos negócios multinacionais](https://www.fon.hum.uva.nl/rob/Courses/InformationInSpeech/CDROM/Literature/LOTwinterschool2006/szabo.best.vwh.net/multi.small.html). As barreiras legais são o custo mais severo de se fazer negócios em muitas jurisdições. Contratos inteligentes podem cortar esse nó górdio de jurisdições. Onde os contratos inteligentes podem aumentar a privacidade, eles podem diminuir a vulnerabilidade a jurisdições caprichosas. Onde os contratos inteligentes podem aumentar a observabilidade ou verificabilidade, eles podem diminuir a dependência desses códigos legais locais obscuros e tradições de fiscalização.

As consequências de um projeto inteligente de contrato no direito e na economia dos contratos, e na elaboração de contratos estratégicos (e vice-versa), foram pouco exploradas. Da mesma forma, suspeito que as possibilidades de redução significativa dos custos de transação na execução de alguns tipos de contratos e as oportunidades de criação de novos tipos de negócios e  instituições sociais com base em contratos inteligentes são vastas, mas pouco exploradas. Os "cypherpunks" exploraram o impacto político de alguns dos novos blocos de construção do protocolo. O campo de Electronic Data Interchange (EDI), no qual elementos de transações comerciais tradicionais (faturas, recibos, etc.) são trocados eletronicamente, às vezes incluindo  criptografia e recursos de assinatura digital, pode ser visto como um precursor primitivo de contratos inteligentes. Na verdade, esses formulários de negócios podem fornecer bons pontos de partida e marcadores de canal para designers de contrato inteligentes.

## Observabilidade e ações ocultas

Uma tarefa importante dos contratos inteligentes, que tem sido amplamente negligenciada pelo EDI tradicional, é crítica para "o encontro das mentes" que está no cerne de um contrato: comunicar a semântica dos protocolos às partes envolvidas. Há ampla oportunidade em contratos inteligentes para "letras miúdas inteligentes": ações executadas pelo software ocultadas de uma das partes na transação. Por exemplo, as máquinas POS de supermercados não informam aos clientes se seus nomes estão ou não sendo vinculados a suas compras em um banco de dados. Os balconistas nem mesmo sabem, e já processaram milhares de transações assim sob seus narizes. Assim, por meio de ação oculta do software, o cliente está dando informações que ele pode considerar valiosas ou confidenciais, mas o contrato foi redigido e a transação foi desenhada, de forma a ocultar as
partes importantes dessa transação do cliente.

Para comunicar adequadamente a semântica da transação, precisamos de boas metáforas visuais para os elementos do contrato. Isso ocultaria os detalhes do protocolo sem abrir mão do controle sobre o conhecimento e a execução dos termos do contrato. Um exemplo primitivo, mas bom, é fornecido pelo software SecureMosiac da CommerceNet. A criptografia é mostrada colocando o documento em um envelope e uma assinatura digital colocando um selo no documento ou envelope. Por outro lado, os servidores Mosaic registram conexões, e às vezes até transações, sem avisar os usuários - ações ocultas clássicas.

## Blocos de construção criptográfica

Os protocolos baseados em matemática, chamados de *protocolos criptográficos*, são os blocos de construção básicos que implementam as compensações aprimoradas entre observabilidade, verificabilidade, privacidade e aplicabilidade em contratos inteligentes. Ao contrário do senso comum, a obscuridade costuma ser crítica para a segurança. Os protocolos criptográficos são construídos em torno de focos de obscuridade chamados chaves. A imensa aleatoriedade desconhecida de uma chave permite que o resto do sistema
seja simples e público. A obscuridade de um grande número aleatório, tão vasto que um palpite de sorte é improvável, se desejado, no tempo de vida do universo, é a base sobre a qual os protocolos criptográficos e, por sua vez, os contratos inteligentes são construídos.

Uma grande variedade de novos protocolos criptográficos surgiu nos últimos anos. O tipo mais tradicional de criptografia é a criptografia de chave secreta, na qual Alice e Bob (nossas partes exemplares em um contrato inteligente) usam uma única chave combinada previamente combinada para criptografar mensagens entre eles. Um problema fundamental que veremos ao longo desses protocolos é a necessidade de manter as chaves em segredo, e a criptografia de chave pública ajuda a resolver isso. Nessa técnica, Alice gera duas chaves, chamadas de chaves privadas e públicas. Ela mantém a chave privada em segredo e bem protegida, e publica a chave pública. Quando Bob deseja enviar uma mensagem para Alice, ele criptografa uma mensagem com sua chave pública, envia a mensagem criptografada e ela descriptografa a mensagem com sua chave privada. A chave privada fornece um "alçapão" que permite que Alice calcule um inverso fácil da função de criptografia que usou a chave pública. A chave pública não fornece nenhuma pista sobre o que é a chave privada, embora elas sejam matematicamente relacionadas. O algoritmo [RSA](http://szabo.best.vwh.net/rsa.html) é o método mais amplamente usado de criptografia de chave pública.

A criptografia de chave pública também possibilita uma ampla variedade de *assinaturas digitais*. Isso prova que um dado (doravante referido apenas como um "objeto") estava em contato ativo com a chave privada correspondente à assinatura: o objeto foi ativamente "assinado" com aquela chave. A assinatura digital provavelmente deveria ter sido chamada de "carimbo digital" ou "selo digital", já que sua função se assemelha mais a esses métodos do que a um autógrafo. Em particular, não é biométrico como um autógrafo, embora a incorporação de uma senha digitada como parte da chave privada usada para assinar às vezes possa substituir um autógrafo. Em muitos países asiáticos, um bloco de madeira entalhado à mão, chamado de "chop", é frequentemente usado em vez de autógrafos. Cada corte é único e, devido ao entalhe único e ao grão da madeira, não pode ser copiado. Uma assinatura digital é semelhante ao chop, uma vez que cada chave recém-gerada é única, mas é trivial copiar a chave se obtida do titular. Uma assinatura digital pressupõe que o titular manterá o segredo da chave privada.

Uma *assinatura cega* é uma assinatura digital e um protocolo de criptografia de chave secreta que, juntos, possuem a propriedade matemática da comutatividade, de modo que podem ser removidos ao contrário da ordem em que foram aplicados. O efeito é que Bob "assina" um objeto, para o qual ele pode verificar sua forma geral, mas não pode ver seu conteúdo específico. Normalmente, a chave da assinatura define o significado do objeto assinado, em vez do conteúdo do objeto assinado, para que Bob não assine um cheque em branco. Assinaturas cegas usadas em instrumentos de portador digital, onde Bob é o agente de compensação, e em [credenciais de Chaumian](http://www.digicash.com/publish/bigbro.html), onde Bob é o emissor da credencial.

O *compartilhamento secreto* é um método de dividir uma chave (e, portanto, controlar qualquer objeto criptografado com essa chave) em N partes, das quais apenas M são necessárias para recriar a chave, mas menos de M das partes não fornecem informações sobre a chave. O compartilhamento de segredos é uma ferramenta potente para distribuir o controle sobre objetos entre os principais.

A [prova interativa de conhecimento zero](http://www.niksula.cs.hut.fi/~haa/nonpub/zeroknowledge.html) é uma alternativa aos métodos de chave pública para identificação de desafio-resposta. Caso contrário, partes funcionando normalmente que têm um incentivo para responder adequadamente ao desafio, mas falham em fazê-lo, não possuem a chave), sem revelar qualquer informação sobre essa chave privada ao desafiante ou a qualquer bisbilhoteiro. ZKIPs são usados atualmente para autenticação e em armas inteligentes para Identificação de Amigo ou Inimigo (IFF).

As informações sobre quem está falando com quem, como as que podem ser encontradas nas contas de telefone, podem ser muito valiosas, mesmo sem registros do conteúdo real. O envio de mensagens confidenciais é necessário para que alguns dos recursos de privacidade das [credenciais de Chaumian](http://www.digicash.com/publish/bigbro.html) e títulos ao portador sejam implementados fortemente em uma rede real. Para fornecer a confidencialidade do tráfego, um mix digital pode permitir que as partes se comuniquem através de uma rede sem revelar seus parceiros aos provedores de rede ou ao mundo exterior. Em uma mixagem, a análise de tráfego por Eve é impedida pela criptografia de boneca russa da mensagem pelo remetente com as chaves públicas de cada operador de mixagem na cadeia e a mixagem de mensagens por cada operadora, de modo que a escuta telefônica panóptica Eve perde o controle das mensagens. Para que o par remetente / destinatário permaneça confidencial, apenas 1 entre N das operadoras precisa ser confiável com suas informações de tráfego local, embora Eva às vezes possa reunir estatísticas sobre um grande número de mensagens entre os mesmos parceiros para eventualmente adivinhar com quem está falando a quem. As partes que se comunicam também podem ser mutuamente anônimas e, com a criptografia normal, não é necessário confiar em outras partes o conteúdo das mensagens. O software "Mixmaster" na Internet implementa a maioria dos recursos de uma mixagem digital [Mixmaster].

## Proteção de Chaves

Até agora, presumimos que partes como a de Alice e Bob são monolíticas. Mas no mundo dos contratos inteligentes, eles usarão agentes
de software baseados em computador e cartões inteligentes para fazer suas licitações eletrônicas. As chaves não estão 
necessariamente ligadas a identidades, e a tarefa de fazer essa ligação acaba sendo mais difícil do que à primeira vista.
Uma vez que as chaves são vinculadas, elas precisam ser bem protegidas, mas as conexões de rede de longa distância são
notoriamente hackers.

Se assumirmos que o invasor tem a capacidade de interceptar e redirecionar quaisquer mensagens no protocolo de rede, como 
é o caso em redes de longa distância, como a Internet. então também devemos assumir, para a prática todos os sistemas
operacionais comerciais, que eles também seriam capazes de invadir computadores clientes, se não comerciantes, e encontrar
quaisquer chaves no disco.

Não há uma solução completamente satisfatória para a segurança de operações de endpoint de ataques baseados em rede, mas
aqui está uma estratégia para praticamente neutralizar esse problema para sistemas baseados em chave pública:

Todas as operações de chave pública são feitas dentro de uma placa de hardware ilegível em uma máquina com uma conexão de 
linha serial muito estreita (ou seja, carrega apenas um protocolo de uso único simples com segurança bem verificada) para 
um firewall dedicado. Essa placa está disponível, por exemplo, na Kryptor, e acredito que o Viacrypt também pode ter uma 
placa compatível com PGP. Isso é econômico para sites centrais, mas pode ser menos prático para usuários normais. Além de 
melhor segurança, tem a vantagem adicional de que o hardware acelera os cálculos de chave pública.

Se a capacidade de Mallet é paralisar fisicamente a máquina, uma forma mais fraca de proteção de chave será suficiente. 
O truque é manter as chaves na memória volátil. Isso torna o PC à prova de ataques físicos - tudo o que é necessário para
destruir as chaves é desligar o PC. Se os backups da chave puderem ser ocultados em um local físico diferente e seguro, isso 
permitirá que o usuário deste PC criptografe grandes quantidades de dados no próprio PC e em redes públicas de computadores,
sem medo de que um ataque físico contra o PC comprometa esse dados. Os dados ainda estão vulneráveis a um "ataque de mangueira 
de borracha" em que o proprietário é coagido a revelar as chaves ocultas. A proteção contra ataques de mangueiras de borracha 
pode exigir alguma forma de compartilhamento de segredo Shamir, que divide as chaves entre diversos sites físicos.

## O "Homem no Meio" e a Teia de Confiança do PGP

Como Alice sabe que tem a chave de Bob? Quem, de fato, pode ser as partes de um contrato inteligente? Eles podem ser definidos
apenas por suas chaves? Precisamos de dados biométricos (como autógrafos, senhas digitadas, varreduras de retina, etc.)?

O pacote de software de criptografia de chave pública "Pretty Good Privacy" (PGP) usa um modelo chamado "a web de confiança".
Alice escolhe *apresentadores* em quem ela confia para identificar adequadamente o mapa entre outras pessoas e suas chaves públicas.
PGP assume a partir daí, validando automaticamente quaisquer outras chaves que tenham sido assinadas pelos apresentadores
designados de Alice.

Existem dois critérios totalmente separados que o PGP usa para julgar a utilidade de uma chave pública:

1) A chave realmente pertence a quem parece pertencer? Em outras palavras, ele foi certificado com uma assinatura confiável?

2) Pertence a um apresentador, alguém em quem você pode confiar para certificar outras chaves?

Tendo sido informado por Alice a resposta à segunda pergunta, PGP pode calcular a resposta à primeira pergunta para
as chaves públicas que Alice coletou.

As chaves que foram certificadas por um apresentador confiável são consideradas válidas pelo PGP. As chaves 
pertencentes a apresentadores confiáveis devem ser certificadas por você ou por outros apresentadores confiáveis. 
Esta "transitividade" introduz um terceiro critério implícito

3) A chave pertence a alguém em quem você pode confiar para apresentar outros apresentadores?

PGP confunde isso com o critério (2). Não está claro se uma única pessoa tem julgamento suficiente para realizar a
tarefa adequadamente (3), nem foi proposta uma instituição razoável para fazê-lo. Este é um dos problemas não resolvidos
em contratos inteligentes.

O PGP também pode receber classificações de confiança e ser programado para calcular uma pontuação ponderada de validade -
por exemplo, duas assinaturas marginalmente confiáveis podem ser consideradas tão confiáveis quanto uma assinatura totalmente
confiável.

Quaisquer chaves no anel de chave secreta de Alice são "axiomaticamente" válidas para o programa PGP de Alice, não 
necessitando da assinatura do apresentador. PGP também assume que Alice, em última análise, confia em si mesma para certificar
outras chaves.

Acredita-se que o PGP causa o surgimento de uma rede de confiança descentralizada e tolerante a falhas para todas as chaves
públicas, mas uma cadeia de introdutores introduzidos enfraquece muito rapidamente, devido à falta de transitividade.

A abordagem de base do PGP contrasta fortemente com os esquemas tradicionais de gerenciamento de chave pública, como o X.509
e o Privacy Enhanced Mail (PEM) relacionado. Esses esquemas padrão subsistem um sistema hierárquico de introdutores chamados
autoridades de certificação (CAs).

## O notário público (ou Tabelião)

Dois atos diferentes são freqüentemente chamados de "notarização". O primeiro é simplesmente quando alguém jura a verdade de
alguma declaração perante um notário ou algum outro oficial com direito a prestar juramento. Isso não exige que o notário saiba
quem é o afiliado. O segundo ato é quando alguém "reconhece" perante um notário que assinou um documento como "seu próprio ato
e ação". Este segundo ato exige que o notário conheça a pessoa que fez a declaração. Assim, por exemplo, a forma de uma
confirmação pode ser mais ou menos assim:

Neste ____ dia de ___ de 19__, compareceu pessoalmente perante mim ____, conhecido por mim e por mim conhecido por ser a
pessoa que assinou o instrumento anterior, e reconheceu que executou o mesmo como seu próprio ato e ação.

No primeiro tipo de ato de notarização, o tabelião apenas atesta que o declarante jurou que a afirmação era verdadeira.
No segundo tipo, o notário realmente atesta que a pessoa que fez o reconhecimento era quem afirma ser.

## Problemas com Certificação

Essas funções de um notário público são substancialmente diferentes da alegada função de herararquias de "autoridades de
certificação" (CAs) no PEM / X.509 e da "rede de confiança" no PGP, para "provar a identidade". Na verdade, os certificados 
gerados por esses sistemas não fazem isso. Em vez disso, um certificado prova que uma reclamação foi feita por uma CA em 
algum momento no passado. A afirmação (implícita) é que uma determinada chave pertencia a uma determinada pessoa naquele momento.
Essa chave não é biométrica como um autógrafo e, portanto, pode ser transferida a qualquer momento. Além disso, falsas alegações
podem ser feitas por uma CA sobre quais chaves um usuário final possui, e o usuário final pode ficar preso sem nenhuma evidência
de fraude de CA; nem a CA tem qualquer maneira de provar que sua afirmação é correta se um usuário final contestá-la. Por outro
lado, é extremamente difícil para os tabeliães falsificarem autógrafos e esperarem se safar com a freqüência necessária para
manter sua reputação profissional.

Tanto a web de confiança PGP quanto os modelos X.509 apresentam mais falhas. Uma única hierarquia enraizada pressupõe uma besta
mitológica chamada de entidade de confiança universal. As hierarquias em geral criam estruturas rígidas que não se encaixam na
maneira como o conhecimento sobre chaves e portadores de chaves, e incentivos para refletir com precisão esse conhecimento, são
distribuídos entre as pessoas no mundo real. Por sua vez, enquanto o PGP distingue entre "Alice possui uma chave" e "Alice pode
ser confiável para certificar uma chave", isso não significa que a segunda afirmação de que Alice pode ser confiável para validar
outro emissor. Há pouca transitividade: ver a chave de Alice certificada por Bob, a quem conheço e confio, pouco me diz sobre se
a certificação de Alice da chave de Charlie está correta. Ver Alice certificada por Bob como apresentadora me diz pouco sobre se
Alice pode ser confiável para certificar outros apresentadores. Isso me diz que sei culpar Alice se sua afirmação estiver errada;
embora esteja longe de estar claro que Alice tem qualquer responsabilidade legal.

Há uma falha ainda mais grave quando a chave pública é usada para assinaturas digitais. Como a reivindicação só foi feita no 
passado, tanto PGP quanto X.509 permitem que o usuário final negue de forma plausível que "assinou" um documento; e, inversamente,
se a chave de uma pessoa for furtivamente roubada ou, por outras razões, nenhuma ação de revogação for tomada, não há como provar
que não "assinou" o documento digitalmente "assinado" com a chave roubada. Finalmente, não existe um acordo legal amplamente
aceito sobre o que está sendo especificamente reivindicado quando alguém "certifica" uma chave, nem há qualquer mecanismo embutido
ou amplamente utilizado para descrever a reivindicação real que alguém está fazendo. CAs do mundo real têm o péssimo hábito de se
isentar de responsabilidade por seus erros ou pelos mal-entendidos que surgirão das alegações muitas vezes vagas e desleixadas,
às vezes implícitas, que fazem. Finalmente, há uma grande variedade de outras afirmações que alguém pode fazer sobre uma chave, 
como "esta chave pertence a um escritório", "esta chave pertence a um servidor", "este detentor da chave tem uma boa classificação
de crédito", "use isto chave para descriptografar sua nova cópia do Microsquish Expel "," esta chave é válida para 100 MB de
downloads de nosso servidor web ", etc. que não são facilitados nem pelo X.509 nem pelo PGP Web of Trust.

Sabemos muito pouco sobre os melhores usos da criptografia de chave pública para estabelecer esses métodos fixos com uma semântica 
restrita. Este autor sugeriu um mecanismo que modifica a rede de confiança PGP para criar um certificado arbitrário com uma forma
aproximadamente a seguinte:

Chave sobre a qual uma reivindicação está sendo feita tipo de reivindicação, em algum formato padrão de uma linha (como tipos MIME)
Descrição de texto simples da reivindicação Carimbo de data / hora digitalmente "assinado", chave de Alice

Em outras palavras, todas as declarações sobre chaves devem ser *explícitas*, prontamente conhecidas pela leitura do próprio
certificado, e nenhum tipo de declaração deve ser arbitrariamente excluído pelo mecanismo. A força legal da afirmação pode 
ser baseada no próprio texto, em vez de interpretações exageradas, obscuras e muitas vezes implícitas sobre o que "certificação"
deve significar. Tipos padrão de reivindicações surgirão, incluindo talvez certificados mais transitivos de "bom juiz do
julgamento" para os quais o software de acompanhamento de cadeia pode ser escrito e credenciais não transitivas "é uma pessoa"
diretamente "vinculadas" à identificação tradicional autenticada por um protocolo de reconhecimento de firma físico que inclui
autógrafos e "assinaturas" digitais. Mais provavelmente, novos e mais úteis tipos de certificados irão evoluir. Deve-se permitir
que esses padrões surjam a partir de uma ampla variedade de usos finais possíveis, bem como a jurisprudência amadureceu ao 
longo do tempo, ao invés de ser ditada por nosso entendimento atual muito inexperiente.

Enquanto isso, existe uma defesa mais prática contra o homem no meio do ataque: anunciar, desde o início e com frequência.
Os usuários de uma rede insegura podem comunicar a integridade de uma chave razoavelmente bem, vinculando-a a um padrão 
persistente de comportamento: por exemplo, postagens em um estilo persistente de um endereço de e-mail persistente, persistência
de uma chave não contestada em um servidor de chaves, etc. Esta é a maneira mais prática e amplamente usada pela qual os 
usuários de PGP ganham confiança nas chaves públicas, e não requer autoridades de certificação ou apresentadores. Aqueles
que anunciam suas chaves amplamente, e aqueles que são bem conhecidos, são mais propensos a ter as chaves vinculadas a suas
pessoas.

## Persona Virtual

"Identidade" dificilmente é a única coisa que queremos mapear para uma chave. Afinal, as chaves físicas que usamos para nossa casa,
carro, etc. não estão necessariamente ligadas à nossa identidade - podemos emprestá-las a amigos e parentes de confiança, fazer
cópias delas etc. Na verdade, no ciberespaço, podemos criar uma "persona" para refletir tais relacionamentos com várias pessoas ou,
em contraste, para refletir diferentes partes de nossa personalidade que não queremos que outras pessoas associem. Aqui está um
possível esquema de classificação para personagens virtuais, apresentado pedagogicamente:

Um *nym* é um identificador que vincula apenas uma pequena quantidade de informações relacionadas sobre uma pessoa, geralmente as
informações consideradas pelo titular do *nym* como relevantes para uma determinada organização ou comunidade. Exemplos de *nyms*
incluem apelidos de boletins eletrônicos, pseudônimos e nomes de marcas. Um *nym* pode ganhar reputação dentro de sua comunidade. 
Por exemplo, um conglomerado pode vender uma grande variedade de nomes de marcas, cada um deles respeitável em seu próprio nicho
de mercado. Com as credenciais de Chaumian, um *nym* pode tirar vantagem das credenciais positivas das outras ninfas do titular,
conforme comprovadamente vinculadas à credencial "is-a-person".

Um *nome verdadeiro* é um identificador que vincula muitos tipos diferentes de informações sobre uma pessoa, como nome de nascimento
completo ou número do seguro social. Como na magia, saber um nome verdadeiro pode conferir um tremendo poder aos inimigos. 
Também pode ter um grande valor econômico entre aqueles que cooperam pacificamente, como no uso do marketing direto para 
direcionar as informações do produto às pessoas com maior probabilidade de se interessar por esses produtos específicos.

*Persona* é qualquer padrão de comportamento permanente, junto com informações agrupadas de forma consistente, como chave(s),
nome(s), endereço(s) de rede, estilo de escrita e serviços fornecidos.

Um *nome respeitável* é um *nym* ou nome verdadeiro que tem boa reputação, geralmente porque carrega muitas credenciais positivas,
tem uma boa classificação de crédito ou é altamente conceituado. As empresas se esforçam para oferecer nomes de marca 
respeitáveis, enquanto profissionais como médicos e advogados se esforçam para ter boas recomendações pessoais de seus nomes.
Pode ser difícil transferir nomes respeitáveis entre as partes, porque a reputação pressupõe persistência de comportamento,
mas essa transferência pode às vezes ocorrer (por exemplo, a venda de nomes de marcas entre empresas).

## Construindo Smart Contracts

As assinaturas cegas podem ser usadas para construir *instrumentos digitais ao portador*, objetos identificados por uma chave única
e emitidos, liberados e resgatados por um agente de compensação. Quando um objeto é transferido, o transferido pode solicitar ao 
despachante para verificar se a chave nunca foi liberada e emitir uma nova chave. O agente de compensação evita a compensação
múltipla de objetos específicos, mas pode ser impedido de vincular objetos específicos a um ou ambos os ginásios de compensação
que transferiram aquele objeto. Esses instrumentos vêm em uma variedade "online", liberada durante cada transferência e, portanto,
verificáveis e observáveis, e uma variedade "offline", que pode ser transferida sem ser liberada, mas só é verificável 
quando finalmente liberada, revelando qualquer liberação nym de qualquer titular intermediário que transferiu o objeto várias
vezes (uma quebra de contrato). A privacidade do agente de compensação pode assumir a forma de desligamento do transferidor,
desligamento do transferidor ou "duplo-cego", em que tanto o transferidor quanto o transferido são desligados pelo agente de
compensação.

O [dinheiro digital](http://www.digicash.com/ecash/about.html) é o principal exemplo de instrumento digital ao portador, no qual o agente de compensação é um banco.
Os protocolos de instrumentos ao portador permitem o pagamento online ao mesmo tempo que respeitam as características desejadas
das notas ao portador, principalmente a imperdoabilidade (via mecanismo de compensação) e a confidencialidade da transferência
(via cega).

Para implementar uma transação completa de pagamento por serviços, precisamos mais do que apenas o protocolo de caixa digital;
precisamos de um protocolo que garanta que o serviço será prestado se o pagamento for feito e vice-versa. Os sistemas comerciais
atuais usam uma ampla variedade de técnicas para fazer isso, como correio certificado, troca face a face, confiança no histórico
de crédito e agências de cobrança para estender crédito, etc. Contratos inteligentes têm o potencial de reduzir significativamente
os custos de fraude e execução de muitas transações comerciais.

Uma *credencial* é uma reivindicação feita por uma parte sobre outra. Uma *credencial positiva* é aquela que a segunda parte prefere
revelar, como um diploma de uma escola de prestígio, enquanto essa parte prefere não revelar uma *credencial negativa*, como uma 
classificação de crédito ruim.

Uma credencial de Chaumian é um protocolo criptográfico para provar que alguém possui afirmações feitas sobre si mesmo por outras
academias, sem revelar ligações entre essas academias. Baseia-se na *credencial "is-a-person", a credencial de nome verdadeiro, 
usada para provar a ligação de ginásios de outra forma não vinculáveis e para evitar a transferência de *nyms* entre 
partes.

Outra forma de credencial é a *credencial de portador*, um instrumento de portador digital em que o objeto é uma credencial.
Aqui, a segunda parte na reclamação se refere a qualquer portador - a reclamação está vinculada apenas ao nome confiável da
organização emissora, não ao *nym* ou nome verdadeiro da parte que possui a credencial.

## Propriedade Inteligente

Podemos estender o conceito de contratos inteligentes à propriedade. A propriedade inteligente pode ser criada incorporando 
contratos inteligentes em objetos físicos. Esses protocolos incorporados dariam automaticamente o controle das chaves para operar
a propriedade à parte que legitimamente possui essa propriedade, com base nos termos do contrato. Por exemplo, um carro pode 
ficar inoperante a menos que o protocolo de desafio-resposta adequado seja concluído com seu proprietário de direito, evitando
o roubo. Se um empréstimo fosse feito para comprar aquele carro e o proprietário deixasse de fazer os pagamentos, o contrato 
inteligente poderia automaticamente invocar uma garantia, que devolve o controle das chaves do carro ao banco. Essa "garantia
inteligente" pode ser muito mais barata e mais eficaz do que um repo man. Também é necessário um protocolo para remover 
comprovadamente a garantia quando o empréstimo for quitado, bem como dificuldades e exceções operacionais. Por exemplo, seria
rude revogar a operação do carro enquanto ele está fazendo 75 na rodovia.

Propriedade inteligente é um software ou dispositivos físicos com as características desejadas de propriedade incorporadas a eles;
por exemplo, dispositivos que podem ser processados de muito menos valor para partes que não possuem uma chave, conforme 
demonstrado por meio de uma prova interativa de conhecimento zero.

Um método de implementação de propriedade inteligente é por meio de dados necessários da operação (OND): dados necessários para 
a operação da propriedade inteligente. Por exemplo, um OND complexo pode ser uma sequência de disparo proprietária necessária
para operar um mecanismo computadorizado, um arquivo CAM necessário para fabricar uma peça especializada, etc. Para evitar o 
roubo de serviço, o ZKIP é necessário para abrir um canal criptografado para o dispositivo. Para evitar o vazamento de OND para
Eve, a detecção de violação combinada com uma chave de homem morto pode ser usada na extremidade do dispositivo do canal.

Também podemos usar e enraizar dispositivos imobilizadores ou destrutivos para frustrar as tentativas de conectar propriedades 
inteligentes.

Uma *garantia inteligente* é o compartilhamento de uma propriedade inteligente entre as partes, geralmente duas partes chamadas de
proprietário e titular da garantia. Esta propriedade pode estar na posse próxima do proprietário ou do segurador, correspondendo
às noções de direito comum de "garantia do artesão" e "garantia do estalajadeiro", respectivamente. As garantias inteligentes
podem ser usadas para garantir linhas de crédito, apólices de seguro e muitos outros tipos de contratos que envolvem propriedade
inteligente.

Como cobrar dívidas? Nenhum banco sábio emprestará, a menos que o credor possa ser coagido a pagar a dívida ou o empréstimo seja 
mais do que coberto por garantias seguras e alguma função conservadora de sua reputação de pagamento integral e dentro do prazo. 
Para todas as partes, tanto o crédito quanto a responsabilidade estão intimamente relacionados e são limitados.

A responsabilidade de uma parte é limitada pelas garantias dessa parte e pela capacidade de dissuadir essa parte por meio de
ameaças de punição por violar contratos (ou seja, cometer crimes conforme definido pelo contrato com a jurisdição). O potencial
para outras ações que uma parte possa tomar que causem responsabilidade, como danos a pessoas ou propriedades de terceiros, 
também precisa ser limitado. Mais sobre isso mais tarde.

Muitas partes, especialmente os novos entrantes, podem não ter esse capital de reputação e, portanto, precisam ser capazes de
compartilhar sua propriedade com o banco por meio de garantias seguras. A garantia é, em um sentido prático, um método de 
compartilhar um pedaço de propriedade entre o "dono do registro" e um "titular da garantia", em vez de a propriedade ter 
estritamente um proprietário. Os ônus são usados em muitas transações de crédito de grande porte, como empréstimos para compra 
de automóveis, hipotecas, empréstimos agrícolas, etc. Eles são impostos pela jurisdição especificada no contrato; geralmente essa 
fiscalização é feita pelo governo e subsidiada pelos contribuintes, em vez de paga pelas partes contratantes. (Na verdade, esse
geralmente é o caso com contratos e direitos de propriedade em geral, a cláusula de execução é um subsídio governamental 
implícito). Uma maneira de implementar uma garantia sem governos é por meio da co-assinatura com o árbitro escolhido em particular
(desde que o árbitro tenha uma boa reputação e o direito contratual de tomar as medidas cabíveis contra você). As garantias 
inteligentes podem expandir muito a privacidade e a segurança de tais acordos.

Como é o caso hoje, os problemas de crédito geralmente serão resolvidos por cartas de advertência escritas de maneira habilidosa
e ameaçadoras e reclamações sobre o rating de crédito de alguém muito antes de a garantia precisar ser invocada. No entanto, a 
garantia precisa ser executável para tornar essas cartas de cobrança confiáveis no longo prazo.

Que tal estender o conceito de contrato para cobrir o acordo a um conjunto pré-arranjado de leis de responsabilidade civil? Essas
leis de responsabilidade civil seriam definidas por contratos entre agências privadas de arbitragem e fiscalização, enquanto os 
clientes teriam uma escolha de jurisdições neste sistema de "governos" de livre mercado. Se essas organizações jurídicas privadas
(PPLs, para abreviar) assumirem a responsabilidade final pelas atividades criminosas de seus clientes, ou precisarem garantir a 
falta de deserção ou pagamentos futuros por parte dos clientes, eles podem, por sua vez, pedir gravames contra seus clientes, seja
com os termos contratuais que permitem a prisão de clientes sob certas condições (por exemplo, se eles cometerem atos 
especificados como criminosos pelo contrato PPL) ou (mais provavelmente para viajantes pelo mundo móvel e clientes com 
pseudônimos virtuais) penhoras inteligentes contra ativos líquidos, como contas bancárias e investimentos carteiras. As 
garantias inteligentes sobre informações, como títulos ao portador digitais, podem ser implementadas por meio de compartilhamento
secreto (duas ou mais chaves necessárias para desbloquear a criptografia).

Outras áreas importantes de responsabilidade incluem responsabilidade do consumidor e danos à propriedade (incluindo poluição). 
São necessários mecanismos para que, por exemplo, os danos causados pela poluição a pessoas ou propriedades alheias possam ser
avaliados, e existam gravames para que o poluidor seja devidamente cobrado e as vítimas pagas. Onde a poluição é quantificável,
como acontece com as emissões de SO2, os mercados podem ser criados para negociar direitos de emissão. Os PPLs teriam gravames 
em vigor para monitorar as emissões de seus clientes e avaliar as taxas onde os direitos de emissão foram excedidos.

Infelizmente, existem alguns perigos em que o dano máximo pode ultrapassar qualquer ônus. Uma boa regra prática aqui é que se o 
risco for contra um terceiro e não puder ser penhorado ou segurado, então os PPLs não devem permitir que seja assumido. Os PPLs 
que permitem que seus clientes assumam tais riscos contra partes não PPL arruinariam sua classificação de crédito. Um exemplo 
desse risco é a construção de uma usina nuclear para a qual nenhuma seguradora está disposta a apresentar cobertura de
responsabilidade. Se uma planta é segura, presumivelmente deve-se ser capaz de convencer uma boa seguradora a cobrir seu potencial
de danos à propriedade de terceiros.

## Conclusão

O dinheiro digital está aqui hoje, e muitos outros mecanismos de contrato inteligentes estão sendo projetados. Até agora,
os critérios de design importantes para automatizar a execução de contratos vieram de campos díspares, como economia e
criptografia, com pouca comunicação cruzada: pouca consciência da tecnologia por um lado e pouca consciência de seus melhores
usos comerciais por outro. A ideia dos contratos inteligentes é reconhecer que esses esforços buscam objetivos comuns, que
convergem para o conceito de contratos inteligentes.


### References:
Oliver Williamson, *The Economic Institutions of Capitalism*

Janet Landa, *Trust, Ethnicity, and Identity*

*The New Palgrave: Allocation, Information, and Markets*

Bruce Schneier, *Applied Cryptography*

*Crypto* and *Eurocrypt* conference proceedings, 1982-1994.

"Crypto Rebels", Wired #2, also cypherpunks mailing list* (mail to majordomo@toad.com with body "subscribe cypherpunks")

Perry H. Beaumont, *Fixed Income Synthetic Assets*

[Frederich Hayek](http://www.xmission.com/~legalize/lf/blurbs/f-a-hayek.htm), The Fatal Conceit

Ming Li & Paul Vitanyi, *An Introduction to Kolmogorov Complexity and Its Applications*

Vernor Vinge, "True Names" (fiction), from *True Names and Other Dangers*

Mixmaster (ptr to web site)

PGP (ptr to web site)

Tim May, "Cyphernomicon"

[David Chaum, "Security Without Identification"](http://www.digicash.com/publish/bigbro.html)

[David Chaum, "Achieving Electronic Privacy"](http://www.digicash.com/publish/sciam.html)

[Agorics web site](http://www.agorics.com/)

[DigiCash web site](http://www.digicash.com/)

