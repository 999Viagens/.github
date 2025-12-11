# Elaboração de Pull Requests

## #1. Mantenha-os pequenos

Manter os Pull Requests (PRs) pequenos é uma arte. É muito tentador reescrever, refatorar, otimizar e reformatar o código durante o desenvolvimento, mas, em geral, os melhores desenvolvedores resistem à tentação de mudar tudo de uma vez. Eles se mantêm focados e concluem o trabalho com o mínimo de alterações no código. Alguns até competem para ter a maior proporção de "linhas excluídas" para "linhas adicionadas". Se a otimização e a refatoração forem necessárias, faça-as separadamente. Não invente desculpas para justificar por que é mais fácil simplesmente colocar tudo em um único PR — isso é preguiça. Em vez disso, invente maneiras de criar PRs menores — isso é criatividade.

## #2. Realize uma autoavaliação

Crie um rascunho de PR e faça uma revisão completa você mesmo — incluindo comentários e tarefas. Depois de finalizar um trecho de código, é muito tentador simplesmente despejar suas alterações em um PR e deixar que outras pessoas encontrem os erros, principalmente se for uma mudança grande que levou alguns dias. Não seja preguiçoso — seja disciplinado, seu trabalho ainda não terminou.

Você também pode usar essa “autoavaliação” para apontar coisas aos seus revisores — “Não tenho certeza sobre esse nome. Você consegue pensar em um melhor?”, “Isso realmente deveria ser anulável? O que você acha?” — muitas vezes, ao escrever essas perguntas, você descobre que, na verdade, consegue respondê-las sozinho e a autorreflexão se torna parte do seu processo de pensamento diário ao programar. Em outras palavras, esse processo de autoavaliação faz de você um desenvolvedor melhor.

## #3. Volte e remova o ruído.

Frequentemente, ao fazer uma autoavaliação, você se depara com um arquivo com apenas alterações de espaços em branco, formatação, importações otimizadas ou alguma alteração de texto que não tem impacto algum relacionado à intenção do PR. Faça um esforço, volte ao seu branch e reverta esses arquivos para como estavam antes. Não importa que você os tenha melhorado ligeiramente — funcionalmente, eles são os mesmos, e o arquivo extra na lista de "arquivos alterados" do PR provoca reclamações do revisor e diminui sua motivação para fazer uma revisão adequada — especialmente em PRs maiores.

Se a formatação for importante, crie um PR separado, implemente um linter, integre-o ao seu CI e formate todo o aplicativo em um único PR grande e complexo. Mas mantenha o ruído longe das mudanças importantes — **respeite o tempo e a energia dos seus revisores.**

Além disso, esse tipo de ruído polui o histórico do git blame, dificultando a navegação no histórico para descobrir as intenções por trás de determinadas alterações em um arquivo.

## #4. Crie um título significativo

Muitas vezes, o título é gerado a partir do nome da ramificação ou do ticket relacionado… a única regra aqui é seguir algum tipo de convenção e fazer com que o título seja curto e significativo; o processo de pensamento é semelhante ao da nomenclatura de ramificações. Seja consistente.

Os Pull Requests são a nova Documentação, e facilitar a navegação no histórico de Pull Requests torna a busca por decisões e processos de pensamento anteriores muito mais fácil.

## #5. Escreva uma descrição útil

Novamente, trate o PR como documentação — documentação que **você realmente leria porque é útil**. Seja o mais completo possível, mas conciso; tente antecipar discussões sendo o mais transparente possível sobre suas intenções e processo de tomada de decisão.

Uma forma útil de promover a inspiração é estabelecer um Modelo de RP. O conteúdo do modelo deve ser acordado e desenvolvido/ajustado com sua equipe ao longo do tempo, mas aqui estão algumas ideias para começar:

* **Visão geral das alterações.** Os pontos a serem abordados aqui geralmente são aqueles que **não constam** no PR — alternativas que você avaliou e descartou. Isso evita possíveis discussões com revisores que podem sugerir coisas que você já tentou.
* **Perguntas/Observações para os revisores.** Há alguma parte do código sobre a qual vocês precisam de conselhos específicos? Há alguma seção do código que pode ser ignorada sem problemas? Talvez vocês tenham renomeado algo e isso tenha afetado vários arquivos, mas sem impacto funcional. Notificar os revisores de que podem ignorar com segurança uma parte do PR será bem recebido.
* **Como testar/demonstrar.** Isso é útil para o controle de qualidade — combinações de usuário/senha que você pode querer usar no ambiente de teste, instruções de configuração/preparação/instalação… qualquer coisa que ajude o revisor a testar as alterações.
* **Anexos: Capturas de tela, vídeos.** Uma imagem vale mais que mil palavras, um vídeo vale um milhão. Nada substitui ver as mudanças em ação — criar uma prova de conclusão também é um documento útil para ter quando chegar o dia da demonstração e você tiver esquecido de se preparar!

## #6. Responda a todos os comentários.

Em qualquer comunicação remota e assíncrona, é importante demonstrar que você viu **pelo menos** um comentário que era para você. Pode ser com uma simples reação com emoji, tudo bem! Nunca ignore um comentário, por menor que seja, especialmente em uma equipe nova. Depois de se familiarizar e criar um bom relacionamento com a equipe, tudo bem, aí sim você pode relevar alguns comentários, porque já existe um entendimento mútuo. Mas no início, seja educado, fe comporte-se da melhor maneira possível.

## #7. Não faça a merge até que todos aprovem.

Falando em boas maneiras, é educado esperar até que todos que fizeram uma sugestão tenham a oportunidade de ouvir sua resposta e avaliá-la. Se você estiver esperando há um tempo relativamente longo, entre em contato com eles discretamente (por e-mail, mensagem instantânea, toque no ombro) e avise que está aguardando.

Na minha opinião, se você está em uma equipe de 3 ou mais pessoas, não é necessário que todos revisem todos os PRs. Elabore um sistema para determinar quem deve revisar cada PR — talvez certas pessoas sejam responsáveis por determinados módulos, talvez quando você for novo na empresa o arquiteto/desenvolvedor sênior revise todos os seus PRs até você se formar, ou talvez vocês usem um sistema de rodízio. Existem muitas maneiras de dividir o trabalho, seja criativo.

---

# Revisando

Algumas das dicas abaixo também se aplicam ao autor ao responder aos comentários.

## #8. Confira o código

Tenha sempre duas cópias de um projeto no seu computador ao mesmo tempo. Uma para o trabalho normal e outra para revisar pull requests. Dessa forma, você pode pausar sua tarefa atual sem qualquer interrupção.

Depois de selecionar a branch, clique em "Build" e deixe o processo de compilação em execução enquanto você volta para o navegador.

## #9. Leia o título e a descrição

Se alguém se deu ao trabalho de escrever um guia para o seu PR, o mínimo que você pode fazer é dedicar um tempo para lê-lo. Portanto, enquanto o projeto está sendo desenvolvido em seu outro projeto clone, leia o ticket vinculado, o título e a descrição do PR — prepare suas expectativas para o que você está prestes a analisar.

## #10. Valide suas sugestões localmente

Quando encontrar algo que possa ser melhorado, tente fazer a alteração em seu clone local. Isso é especialmente importante para quem está começando em um projeto. Não há nada mais constrangedor do que sugerir uma alteração de código que não é possível e nem sequer compila. Além disso, você terá uma melhor compreensão do código quando ele estiver em sua IDE e, à medida que fizer alterações, poderá se inspirar para realizar uma refatoração maior ou perceber que sua sugestão teria sido inútil. Ambos os resultados são igualmente importantes e valiosos, além de simplesmente validar sua sugestão.

Após verificar se a sua sugestão é pelo menos possível, não desperdice o esforço já realizado: copie as alterações de código e insira-as em um bloco de código no comentário do PR para que o autor possa copiá-las diretamente para o seu branch.

## #11. Converter sugestões extensas em uma solicitação de pull request

Se você perceber que sua sugestão ficou muito extensa, não desperdice seu esforço: crie um branch a partir do branch original e faça um PR para mesclar com o PR original. Este novo PR não precisa de todos os detalhes de um PR normal, pois é apenas um comentário mais elaborado, mas oferece um espaço separado para discussão sobre uma mudança maior. Essa mudança pode ser testada pelo autor original e, se tudo correr bem, finalmente mesclada ao PR principal.

## #12. Resista à tentação de comentar

O mais difícil em fazer comentários é resistir à tentação de comentá-los. A chave para a contenção é ser tão rigoroso consigo mesmo quanto você será com os outros. Se você alguma vez se perguntar o quão eficaz você é como avaliador, revise todos os seus comentários e verifique quantos deles resultaram em sugestões bem recebidas e implementadas com o mínimo de idas e vindas.

Aqui estão algumas dicas úteis para melhorar seus comentários:

## #13. Se você não tiver uma alternativa concreta, não faça um comentário.

Se você simplesmente não gosta de algo, apresente algo melhor e defenda seus argumentos; caso contrário, fique calado.

❌ “Hum, é, eu simplesmente não gostei do que você fez aqui.”
❌ “Eu realmente não gosto dessa abordagem.”
✅ 🦗🦗🦗🦗🦗 (Silêncio)

## #14. Seja confiante, não preguiçoso.

Não use palavras como "talvez", "não sei", "e se", "não tenho certeza"... nada que implique dúvida. Se você não tem certeza, reflita sobre si mesmo — por que você não tem certeza? Faça alguns experimentos ou pesquisas... volte confiante.

❌ “Não sei, mas se você fizer essa alteração, pode ser que fique melhor. Confira e veja o que acha.”

> Preguiçoso: Você não sabe? Não comente até saber.

> Confiante: se você sabe, não diga que não sabe — seja confiante, apresente sua sugestão de forma clara e explique **por que** ela é melhor, **sem** mencionar sua própria opinião (veja a próxima seção sobre Estilo).

✅ “Se você refatorar isso em uma função inline como esta [bloco de código], o código fica menor e mais idiomático. Também evita duplicação de código. No entanto, não é tão fácil de simular durante os testes.”

Percebeu aquela última parte sobre ser mais difícil de testar? Não há nada de errado em delinear e antecipar os aspectos negativos das suas sugestões. Isso demonstra que você está pensando de forma objetiva e racional — nenhuma solução é perfeita.

## #15. Imite as convenções de estilo antes de alterá-las.

As pessoas têm um apego estranho ao estilo e formam opiniões muito fortes rapidamente. Ao entrar em uma nova equipe, os membros antigos costumam defender o status quo do projeto, enquanto os novos membros frequentemente expressam abertamente como "fizeram melhor/de forma diferente em seu projeto anterior".

**Supere isso.**

Adaptar-se a um estilo já existente lhe renderá pontos extras com sua nova equipe e os deixará mais abertos às suas sugestões sobre assuntos mais importantes: escolha do SDK, decisões arquitetônicas, padrões e práticas. Depois de dominar o estilo deles sem reclamações, você perceberá que eles serão um público mais receptivo quando você sugerir uma modernização do estilo.

## #16. Ser meticuloso é um bom sinal

Se seus colegas revisarem seu comunicado à imprensa e você receber apenas comentários sobre correções de estilo, isso pode parecer preciosismo, o que pode ser frustrante.

Mas veja por este ângulo: os revisores estão tendo dificuldade em encontrar problemas **reais** no seu código.

Uma boa resposta para críticas minuciosas é destacar, educadamente, a ineficiência de se apegar a detalhes quando existem ferramentas de desenvolvimento integrada (IDEs) que lidam com 90% das decisões de estilo automaticamente. Geralmente, a ausência de verificações de estilo automatizadas é sintoma de preguiça, falta de motivação ou má gestão — então, crie-as você mesmo!

> "Ops, eu não sabia dessa regra de estilo 😬 desculpe. Ei, você poderia me indicar algum guia de estilo no Confluence/wiki/readme?"

> "Ok, e se eu criar um PR separado com todas essas regras que você mencionou? Vou adicionar todos os comentários que receber a esse documento para que nosso estilo fique documentado e possa permanecer consistente."

> "Ops, desculpe, já é a quadragésima vez que ignoro isso. Alguém se importaria se eu criasse uma regra de linting para isso? Eu poderia adicioná-la à IDE para que fosse detectada durante a codificação, ou talvez a um hook do Git para que fosse detectada antes do push, ou até mesmo a um bot de CI que analisaria o PR e faria um comentário diretamente."

## #17. Leve fios longos para uma sala de reuniões.

Em algum momento da sua carreira, você se envolverá em uma discussão acalorada sobre um comentário em um comunicado de imprensa. A chave é interromper a conversa, acalmar os ânimos e, em seguida, escrever um e-mail para a pessoa com o seguinte teor:

> Ei, idiota!
>
> Desculpe pela discussão acalorada que estamos tendo na assessoria de imprensa. As coisas estão saindo um pouco do controle e acho que é hora de nos reunirmos por telefone ou pessoalmente, talvez com nosso superior imediato ou outros membros da equipe, e resolvermos isso da maneira tradicional. Não se apresse em responder. Podemos retomar o assunto amanhã, depois de refletirmos melhor.
>
> Sinceramente seu,
> Idiota.

O segredo é romper com o ciclo infantil de abusos induzido pelo Twitter e marcar um encontro presencial. As pessoas nunca são tão brutais ou rudes pessoalmente quanto online. Certifique-se de chegar à reunião com a maior calma, com seus argumentos e contra-argumentos bem fundamentados, mas, acima de tudo, mantenha a objetividade. Vá para a reunião com o objetivo de encontrar a melhor solução, não para impor sua vontade.

## #18. Mantenha o tom de voz uniforme

Criar um Pull Request é, por definição, convidar à crítica. Portanto, antes de mais nada: seja crítico. Questione, provoque e desafie — mas faça isso profissionalmente, não pessoalmente.

Use emojis para momentos divertidos,
✅ “Eba! Você usou o Flow 🤩”

Não use emojis numa tentativa transparente de encobrir sua completa falta de tato.
❌ “Usamos espaços neste projeto. Mude isso. 🥳 🚀”

Evite “você”…
❌ “Você esqueceu uma variável aqui”

… tente “nós”
✅ “Está faltando uma variável aqui”

Ou voz passiva em vez disso.
✅ “Há uma variável faltando aqui: [bloco de código]”

Presuma que as pessoas têm boas intenções. Mesmo que você tenha 100% de certeza de que elas estão sendo maldosas, há 10% de chance de você estar errado. Tente encontrar uma maneira de internalizar os comentários e evitar que a situação se agrave.

## #19. Sem Pull Requests de emergência

Os Pull Requests se tornaram populares por dois motivos:

1.  **Comunicação assíncrona.**
2.  **Garantia de Qualidade.**

Se você absolutamente precisa mesclar uma branch nos próximos 10 minutos, não envie uma mensagem pedindo para as pessoas revisarem **agora mesmo**, apenas mescle. Não se preocupe em criar um PR só por causa do processo — você acaba de interromper todo mundo e pedir que façam uma revisão medíocre — anulando os dois principais benefícios de um PR. Se você tem uma branch que precisa ser mesclada em um curto período de tempo, interrompa uma pessoa e faça programação em dupla ou simplesmente mescle e aceite a perda de qualidade.

Pull Requests são uma convenção incrível. As dicas acima raramente se aplicam a todos os projetos; é mais importante que a equipe trabalhe em harmonia do que ter regras e processos rígidos. Seja flexível e gentil, mas também confiante e disciplinado. Seja professor e aluno. Dê e receba.

Se a sua ideia de mudança for bem-intencionada, bem fundamentada, bem escrita e você liderar pelo exemplo, as pessoas o seguirão.
