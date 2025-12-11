# ✍️ Reflexões sobre Etiqueta e Boas Maneiras em um Pull Request

Olá a todos,

Como desenvolvedores/engenheiros de software, quando queremos escrever sobre algo, focamos principalmente nos desafios técnicos, já que são fáceis de descrever e não apresentam muitas áreas cinzentas. Para este PR, quero mudar um pouco essa abordagem e focar mais no lado da **interação humana**. Tentarei abordar a **etiqueta e as boas maneiras** em um pull request.

Criar, revisar e gerenciar pull requests é um assunto subjetivo; cada equipe de desenvolvimento deve encontrar suas próprias melhores práticas. Portanto, neste artigo, vou apresentar algumas das maneiras que usamos na 999viagens para aprimorar nossos pull requests.


---

## 1. Princípio da Responsabilidade Única de uma Solicitação de Pull Request

Aplicar o princípio da responsabilidade única às solicitações de pull request é sempre uma boa ideia.

Tente não incluir conteúdo adicional no PR. Por exemplo, não corrija erros de digitação que não sejam relevantes para o contexto atual, nem adicione pequenas correções de bugs a uma funcionalidade. Dessa forma, você consegue descrever seu objetivo com clareza e evitar confusões. Você também elimina a possibilidade de uma alteração depender da outra.

## 2. Título e Descrição (e Modelos)

O **título e a descrição** são o primeiro lugar onde você pode informar seus colegas de equipe sobre as mudanças. Os títulos dos comunicados de imprensa podem ser rastreados por meio de buscas, portanto, adicionar algumas informações importantes ao título seria útil.

A descrição de um PR deve sempre ser preparada com a mesma atenção, independentemente de a alteração ser pequena ou grande. Revisar um pull request exige que o revisor mude seu foco. Há um minuto você estava olhando para maçãs e agora está olhando para laranjas. Para facilitar essa mudança de contexto, **a descrição do PR é nossa principal ferramenta**. Você pode incluir qualquer coisa na descrição, como tarefas do Jira, logs de erros, elementos visuais do design, etc. **Não limite sua imaginação na hora de descrever o conteúdo; cada detalhe importa.**

Tenha sempre em mente que qualquer pessoa pode ler seu PR a qualquer momento. Portanto, não presuma que este PR se destina apenas à situação atual e aos revisores atuais. **Você está deixando um registro do histórico do seu código. Descreva tudo com essa perspectiva.**


Agradeço a todos pela pesquisa e pela criação deste modelo para a equipe 🚀

---

## 3. Maneiras de Tornar Seu Pull Request Mais Compreensível

Em projetos de longa duração com bases de código extensas, é provável que você tenha uma estrutura modular.

* Se você alterou partes do código que afetam o projeto como um todo, seria interessante **explicar o motivo dessa decisão** e alertar os revisores para que sejam mais cuidadosos. É responsabilidade do autor notificar os revisores e manter o projeto seguro.
* **Comentar as linhas de código no seu PR** é outra boa prática. Eu gosto de incluir links para a **documentação oficial**, **Stack Overflow** e **artigos** nas linhas relacionadas que resolvem algum bug estranho ou trazem um conceito totalmente novo.
* Outra boa prática é **agendar uma reunião** (online) após a criação do PR para compartilhar o conteúdo. **Seja humilde**. Para PRs longos, isso pode ser útil para direcionar seus colegas sobre trechos de código que você gostaria que fossem revisados.
* É **dever do autor testar o código** antes de enviar o PR. Não apresente código que não funciona aos seus colegas de equipe. Mostre respeito por eles.
* Se você alterou algo importante no PR depois que alguns revisores já o aprovaram, **não se esqueça de avisar** os colegas que já o aprovaram para que revisem novamente.

---

## 4. Dicas de Linguagem e Atitude

* Tanto os revisores quanto o autor devem ser **educados** nos comentários. Não hesite em usar **emojis e reações** para descontrair o ambiente 🙂.
* Lembre-se de que **nada é pessoal nos PRs**. Não leve os comentários para o lado pessoal. Os comentários se concentram no código atual.
* Ao deixar ou responder comentários, procure não usar poucas palavras. Tente usar **frases completas** sempre que possível.
* Quando discordar de algo, **apresente uma abordagem alternativa** para evitar discussões improdutivas.
* Quando sua sugestão for complexa demais para ser explicada, considere **criar uma solicitação de pull request para uma solicitação de pull request já existente**. Adote essa prática como um bom hábito.

---

## BÔNUS: Abordagens Técnicas

* Você deve **executar seus testes unitários** antes de criar o PR. Melhor ainda, a equipe deve ter uma etapa de **integração contínua (CI)** que os execute. Isso economiza o tempo de todos os revisores.
* Você deve usar **ferramentas de lint** para manter seu código alinhado com os estilos da equipe. Uma etapa de CI pode executar verificações de lint no PR assim que ele é criado, permitindo que você corrija erros de estilo antes que seus colegas os apontem.

Como cada equipe tem suas próprias maneiras, você pode encontrar mais conselhos nos links abaixo:

* [https://github.blog/2015-01-21-how-to-write-the-perfect-pull-request/](https://github.blog/2015-01-21-how-to-write-the-perfect-pull-request/)
* [https://medium.com/google-developer-experts/how-to-pull-request-d75ac81449a5](https://medium.com/google-developer-experts/how-to-pull-request-d75ac81449a5)
* [https://github.com/thoughtbot/guides/tree/main/code-review](https://github.com/thoughtbot/guides/tree/main/code-review)
* [https://gist.github.com/mikepea/863f63d6e37281e329f8](https://gist.github.com/mikepea/863f63d6e37281e329f8)
* [https://github.community/t/best-practices-for-pull-requests/10195](https://github.community/t/best-practices-for-pull-requests/10195)
* [https://developers.google.com/blockly/guides/modify/contribute/write_a-good-pr](https://developers.google.com/blockly/guides/modify/contribute/write_a-good_pr)
