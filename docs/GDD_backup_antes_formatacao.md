# A Espada Perdida --- Documento de Design do Jogo (GDD)

**Versão:** 0.1 --- documento de trabalho
**Estado:** decisões aprovadas e pontos em aberto identificados
**Motor:** Godot 4
**Plataforma de desenvolvimento:** Android
**Formato:** jogo 2D offline, com salvamento local

> Este documento reúne as decisões aprovadas até agora. Ideias
> identificadas como provisórias ou em aberto não devem ser tratadas
> como cânone definitivo sem nova aprovação.

## 1. Visão do jogo

*A Espada Perdida* é uma pequena aventura de fantasia sombria em pixel
art. O jogador explora ruínas antigas tomadas pela floresta, investiga
sinais de uma influência sobrenatural e procura uma espada ancestral
ligada a um selo que está enfraquecendo.

O objetivo do projeto é criar uma aventura completa --- com começo,
desenvolvimento e conclusão --- enquanto aprendemos a desenvolver jogos
no Godot 4, usando o Codex para tarefas pequenas e revisáveis.

## 2. Pilares de design

-   **Exploração com propósito:** o ambiente conta parte da história por
    meio de caminhos, ruínas, inscrições, animais e pistas.
-   **Mistério coerente:** os segredos têm respostas definidas pelos
    criadores, mesmo quando o jogador ainda não as conhece.
-   **Consequências humanas:** personagens falíveis tomam decisões
    difíceis sem serem reduzidos a heróis perfeitos ou vilões simples.
-   **Escopo controlado:** priorizar uma experiência curta e concluída
    em vez de um mundo enorme inacabado.
-   **Aprendizado seguro:** implementar em etapas, revisar mudanças e
    testar no Godot antes de ampliar o projeto.

## 3. Direção visual e atmosfera

**Aprovado:** - Arte 2D em pixel art. - Fantasia sombria. - Ruínas
antigas cobertas pela floresta. - Tons terrosos e azuis escuros. -
Interface medieval discreta. - A espada antiga/perdida como elemento
central da narrativa.

A aparência exata dos cenários, personagens, criaturas, efeitos e
interface ainda será desenvolvida. Referências visuais conceituais não
são assets finais.

## 4. Câmera e controles

**Aprovado:** - Câmera em visão de cima (*top-down*). - Movimentação em
oito direções: cima, baixo, esquerda, direita e diagonais. - Exploração
direta do cenário.

O esquema definitivo de teclas/botões e a adaptação dos controles à
plataforma serão definidos durante a implementação.

## 5. Escopo da primeira versão

**Aprovado:** - Três áreas principais. - Um encontro sobrenatural
marcante. - Um desafio ou confronto final. - Uma aventura com começo,
desenvolvimento e conclusão. - Jogo offline, com foco em salvamento
local.

### Estrutura inicial proposta

1.  **Floresta em ruínas:** apresentar a movimentação, a exploração e os
    sinais de que os animais estão se comportando de forma estranha.
2.  **O pesquisador e as inscrições:** conhecer o estudioso, descobrir
    pistas e vivenciar o primeiro encontro sobrenatural. O jogador não
    precisa ser obrigado a lutar se houver uma maneira plausível de
    evitar a criatura.
3.  **O antigo selo:** investigar a perturbação, alcançar o desafio
    final e concluir a missão ligada à espada perdida.

Essas áreas são uma estrutura de trabalho, não um mapa final. A
disposição exata e o conteúdo de cada área podem mudar conforme o jogo
for prototipado.

## 6. Protagonista

O protagonista é um antigo explorador de ruínas que abandonou a
profissão depois de uma expedição traumática.

Durante aquela expedição, ele ativou ou rompeu um mecanismo antigo para
salvar o grupo de um perigo imediato. O mecanismo fazia parte de uma
contenção que mantinha uma presença desconhecida presa. Ao rompê-lo, uma
força desconhecida atingiu a expedição e provocou uma tragédia.

Não foram encontrados corpos nem sobreviventes confirmados. O
protagonista não sabe o que aconteceu aos companheiros e acredita que
sua decisão causou a tragédia. O destino dos companheiros permanece em
aberto.

### Personalidade e arco

-   Reservado com desconhecidos.
-   Usa ironia e humor seco quando está desconfortável ou tenta evitar
    assuntos dolorosos.
-   Demonstra afeto principalmente por ações.
-   Torna-se protetor com quem conquista sua confiança.
-   Pode hesitar por um instante diante de situações que lembram a
    tragédia antiga; isso representa trauma, não covardia.
-   Seu arco envolve aprender a agir apesar do medo e a confiar nos
    outros, em vez de assumir sozinho toda a responsabilidade.

### Aparência

Silhueta de aventureiro/sobrevivente: capa assimétrica, couro remendado,
ferramentas no cinto, equipamento reaproveitado, roupas práticas e
gastas, marcas discretas e reparos visíveis. Não deve parecer um
cavaleiro impecável.

### Objeto pessoal

O protagonista guarda uma lembrança ligada aos companheiros
desaparecidos. A forma exata ainda não foi definida. Por enquanto, não
possui poderes ou função mecânica estabelecida.

O nome do protagonista ainda será escolhido. Ele terá uma identidade
fixa, em vez de ser um avatar totalmente personalizável.

## 7. O mundo e a perturbação

A aventura começa numa região compacta de floresta e ruínas antigas. A
influência sobrenatural manifesta-se de forma desigual: alguns animais
ficam agitados ou agressivos, outros fogem ou parecem desorientados, e
certas espécies parecem atraídas pelas ruínas.

Nem todos os animais se tornam agressivos. Comportamentos possíveis
incluem: - pássaros silenciando de repente em determinadas áreas; -
rastros cruzando trilhas em horários incomuns; - marcas recentes de
garras em locais improváveis; - animais abandonando territórios; -
predadores reagindo com agressividade incomum; - criaturas fugindo ou
parecendo desorientadas; - certas espécies aproximando-se das ruínas.

Esses sinais devem gerar curiosidade sem explicar cedo demais a causa.

## 8. O pesquisador e as inscrições

O protagonista encontra por acaso um estudioso que investiga inscrições
antigas nas ruínas. O pesquisador é cauteloso e desconfiado, mas
sincero. Conhece registros e inscrições melhor que o protagonista, porém
não compreende totalmente o que está despertando.

As inscrições podem estar danificadas, ilegíveis ou mudar gradualmente.
Durante o primeiro evento sobrenatural: - surge um sussurro
incompreensível vindo das pedras; - inscrições brilham brevemente; - um
pequeno fragmento de pedra cai; - a floresta do lado de fora fica em
silêncio; - uma criatura aparece à entrada das ruínas e se comporta de
modo anormal.

O estudioso admite que não entende completamente o fenômeno. Mais tarde,
ele poderá oferecer evidências sólidas de que o que o protagonista
suspeita não é apenas trauma ou imaginação, sem identificar a entidade
ou explicar a marca sobrenatural.

## 9. A influência e o primeiro encontro

A influência sobrenatural tem uma relação simbiótica parasitária com
alguns hospedeiros: usa a vitalidade do hospedeiro para permanecer
ligada a ele. Essa verdade não é conhecida no início pelo protagonista
nem pelo pesquisador.

No primeiro encontro, se as condições narrativas forem satisfeitas, a
influência pode abandonar a criatura quando ela chega a um nível crítico
de vida, antes do golpe fatal. Derrotar uma criatura em combate (reduzir
sua vida a zero) e libertar a influência são eventos diferentes.

Nem todos os hospedeiros reagem da mesma forma. Dependendo da espécie,
do estado e das circunstâncias, a influência pode sair, resistir ou não
se manifestar da mesma maneira. Alguns hospedeiros podem morrer antes de
qualquer libertação.

A libertação não cura instantaneamente o animal. Ele pode continuar
ferido, assustado ou exausto. Livre da influência não significa dócil ou
inofensivo: seu comportamento depende da espécie, ferimentos, medo,
exaustão, território, ameaças e rotas de fuga. Na primeira versão, o
jogador poderá observar, dar espaço e permitir que o animal fuja;
tratamento ou cura ativa ficam fora do escopo inicial.

### Resíduo e marca

Depois de abandonar um hospedeiro, a influência deixa por um tempo um
resíduo físico em pedras ou no solo. A aparência visual proposta é uma
mancha escura irregular, semelhante a sombra ou líquido, com pequenas
partículas azul-violeta discretamente luminosas. Pode parecer mover-se
por um instante antes de desaparecer. Essa aparência ainda não é um
asset final.

Enquanto o resíduo está desaparecendo, uma pequena parte toca ou entra
no protagonista e deixa uma marca sobrenatural permanente em sua
aparência. A marca confirma que algo sobrenatural aconteceu, mas não
identifica a presença nem revela sua intenção.

A marca não concede automaticamente poderes e não confirma que o
protagonista foi escolhido, nem que exista uma ligação direta com a
espada ou com uma entidade específica. Sua natureza e implicações
continuam em aberto.

## 10. A espada perdida e o selo

A espada antiga está ligada a uma prisão ou selo que contém uma presença
perigosa. Seu desaparecimento ou remoção enfraqueceu a contenção. Ela
pode ser usada contra a ameaça caso o selo falhe.

Ainda é necessário definir: - por que a espada foi perdida; - como
exatamente a espada interage com o selo; - o que é necessário para
restaurar, alterar ou romper a contenção; - qual foi o custo pessoal da
contenção original; - o que ocorreu com o antigo guardião; - quem ou o
que está preso.

A espada não deve ser tratada como uma solução mágica para todos os
problemas. O seu significado histórico e moral pode ser mais complexo do
que a lenda popular sugere.

## 11. As três entidades

Os conceitos de **Caos**, **Ordem** e **Equilíbrio** são os nomes de
trabalho para três entidades cósmicas equivalentes em importância e
poder. Os nomes verdadeiros ainda serão definidos. Nenhuma delas deve
ser automaticamente classificada como boa ou má.

### Caos

Representa ruptura, mudança, transformação e possibilidade. Pode
libertar povos oprimidos e permitir crescimento, mas também destruir
estruturas, identidades, vínculos e vidas.

### Ordem

Representa estruturas, continuidade, limites e estabilidade. Pode
proteger comunidades e impedir que tudo seja decidido pela força, mas
também sufocar liberdade e perpetuar sistemas injustos.

### Equilíbrio

Intervém nas relações entre forças para impedir que uma delas domine ou
exclua completamente a outra. Isso não significa manter sempre
quantidades iguais nem agir com neutralidade moral. Em certas
circunstâncias, pode aceitar custos terríveis para preservar a
possibilidade de coexistência.

Equilíbrio é uma figura de intriga: leva informações de um lado ao
outro, pode forjar evidências e manipular conflitos. Ordem e Caos
acreditam que podem usar Equilíbrio em benefício dos próprios planos,
sem perceber que também podem estar sendo manipulados. Nenhum deles deve
ser retratado como ingênuo, e os planos de Equilíbrio não são
infalíveis.

É impossível determinar com confiança se o remorso demonstrado por
Equilíbrio é sincero, estratégico ou as duas coisas. Sua consciência e
sua forma de perceber a existência não precisam corresponder à
psicologia humana.

As três entidades não podem ser reduzidas a uma hierarquia simples. Uma
hipótese de trabalho é que eliminar permanentemente as outras duas
também comprometeria as condições que sustentam a própria natureza de
qualquer uma delas; essa regra ainda precisa de validação.

## 12. O antigo guardião

Séculos antes da aventura, um guardião estrangeiro foi acolhido por uma
comunidade e construiu vínculos com seus habitantes ao longo do tempo. A
relação era afetuosa, mas não perfeita: havia conflitos, limitações e
falhas.

Ele queria proteger a comunidade, não conquistar fama ou poder. Diante
de uma crise ligada a uma antiga passagem, escolheu ficar e defender as
pessoas. Ao permanecer, porém, a batalha chegou até a comunidade e
muitos morreram antes que ele recebesse a espada usada para conter o
campeão de uma entidade.

O guardião acabou aceitando que a vitória exigia um custo pessoal e
compreendeu que conter uma ameaça era diferente de matá-la. Os detalhes
concretos da concessão, do custo e do selo continuam em aberto.

A lenda popular pode dizer que ele derrotou o mal com uma espada divina.
A verdade pode ser mais complexa: talvez tenha contido algo em vez de
destruí-lo, e a contenção pode ter implicações morais. Isso é uma
direção narrativa, não uma resposta definitiva.

### Relação entre Ordem, Caos e Equilíbrio na história antiga

Uma direção proposta é que a comunidade tivesse leis e tradições
rígidas, alinhadas com a Ordem, e que a espada tenha sido concedida pela
própria Ordem --- não por Equilíbrio. Equilíbrio pode ter incentivado
Caos a agir naquela região para impedir uma dominação excessiva da
Ordem.

Ainda é preciso decidir se as tradições se tornaram injustas e impediam
mudanças necessárias, ou se a comunidade não era especialmente injusta e
a intervenção ocorreu por razões estratégicas mais amplas. Não presumir
que toda tradição é opressora nem que a intervenção de Caos foi justa.

### Distinções importantes

-   O ser selado não é necessariamente uma das três entidades.
-   Pode ser uma arma, instrumento, agente ou servo poderoso de uma
    delas.
-   O campeão de uma entidade e a criatura selada são conceitos
    distintos até que a história estabeleça uma ligação.
-   Não definir prematuramente a identidade do campeão, seus objetivos
    ou sua relação com a criatura.

## 13. Estrutura narrativa proposta

1.  **Retorno às ruínas:** exploração, controles e primeiros sinais da
    perturbação.
2.  **Encontro com o pesquisador:** inscrições, pistas e divergências
    entre o conhecimento acadêmico e a experiência de campo.
3.  **Primeiro encontro sobrenatural:** criatura influenciada,
    possibilidade de evitar ou enfrentar o perigo, libertação da
    influência e marca no protagonista.
4.  **Investigação do selo:** novas evidências, vestígios do guardião e
    indícios de que a história popular está incompleta.
5.  **Conclusão:** desafio final e resolução da missão principal,
    revelando apenas parte da verdade cósmica.

Essa sequência é um esqueleto narrativo para orientar o desenvolvimento;
os acontecimentos e a conclusão exata ainda precisam ser planejados.

## 14. Mecânicas de jogo

### Aprovadas

-   Exploração em visão de cima.
-   Movimentação em oito direções.
-   Combate em tempo real simplificado.
-   Uma aventura curta com três áreas principais, um encontro
    sobrenatural marcante e um desafio final.

### Proposta inicial para o combate

Começar com movimento, ataque básico, vida do protagonista, vida do
inimigo, comportamento simples de perseguição/ataque e condições de
vitória/derrota. Adicionar habilidades ou sistemas mais complexos
somente se necessários para a aventura.

O método exato de ataque, esquiva, dano, cura, controles e interface
ainda será definido.

### Investigação

Usar elementos do cenário, inscrições, marcas e vestígios como pistas. O
jogador deve conseguir descobrir coisas observando o mundo, sem depender
apenas de longos diálogos.

### Progressão

Não há sistema de classes, árvore de habilidades, economia profunda ou
personalização avançada aprovado para esta versão. Evitar acrescentá-los
antes de haver uma necessidade clara.

## 15. Áudio

Proposta inicial: música e efeitos discretos que reforcem a exploração,
o silêncio súbito da floresta e os momentos sobrenaturais. A direção
sonora definitiva ainda será definida.

## 16. Escopo fora da primeira versão

Para proteger o objetivo de concluir uma aventura pequena, ficam fora do
escopo inicial: - multiplayer ou MMO; - mundo aberto extenso; - sistemas
profundos de classes e habilidades; - companheiros complexos; -
economia, mercado, guildas e guerras; - narrativa com muitas
ramificações; - tratamento avançado de animais; - grandes sistemas que
não sejam necessários para concluir a aventura.

Essas exclusões são limites de escopo da primeira versão, não uma
afirmação de que tais ideias jamais poderão existir em outros projetos.

## 17. Plano técnico e fluxo de trabalho

-   Motor: Godot 4.
-   Projeto offline com foco em salvamento local.
-   Manter cenas, scripts, assets, dados e documentação organizados em
    pastas apropriadas.
-   O GDD deverá ficar em `docs/GDD.md`.
-   Trabalhar com o Codex em tarefas pequenas, explícitas e revisáveis.
-   Abrir o projeto no Godot depois das alterações para validar o
    comportamento.
-   Preservar a cena funcional existente.
-   Não apagar arquivos, descartar alterações, fazer commits ou enviar
    mudanças ao GitHub sem autorização explícita.
-   A implementação deve ser simples o suficiente para o usuário
    entender e aprender com ela.

## 18. Critérios de conclusão

A primeira versão será considerada concluída quando: - for possível
iniciar e terminar a aventura; - a movimentação e a exploração
funcionarem; - houver interação com os elementos narrativos
necessários; - o encontro sobrenatural funcionar de forma
compreensível; - o desafio final e a missão da espada tiverem uma
conclusão; - não houver erros bloqueadores conhecidos; - o salvamento
local estiver implementado e testado, caso seja mantido como requisito
da versão; - o escopo continuar pequeno e coerente.

## 19. Questões em aberto

As seguintes decisões ainda não devem ser presumidas: - nome do
protagonista; - forma da lembrança dos companheiros; - nomes verdadeiros
das três entidades; - identidade e intenção do ser selado; - identidade
do campeão e sua relação com o ser selado; - razão exata para a espada
ter sido perdida; - funcionamento preciso do selo e custo da
contenção; - destino do antigo guardião; - natureza e consequências da
marca sobrenatural; - história e regras da comunidade antiga; -
conclusão exata da aventura; - layout dos mapas, controles definitivos,
detalhes do combate e duração total.

## 20. Princípio orientador

> Não vamos criar mistérios apenas para escondê-los do jogador. Vamos
> criar verdades que mereçam ser descobertas.

A aventura deve funcionar por si só e, ao mesmo tempo, revelar
fragmentos de um universo maior. O protagonista não é perfeito, as
entidades não são simplesmente boas ou más, e o jogador deve descobrir a
verdade por meio de consequências, vestígios e escolhas significativas.
