## Descrição

* O que este PR faz? (Ex: Adiciona a funcionalidade X, Corrige o bug Y, Refatora o serviço Z)
* Qual problema ele resolve?
* [Link para a Issue/Task relacionada]

## Tipo de Mudança

* [ ] Feature (Nova funcionalidade)
* [ ] Bugfix (Correção de um problema)
* [ ] Refactor (Melhoria de código sem mudança funcional)
* [ ] Docs (Apenas mudanças na documentação)

---

## 🧐 PRÁTICA DE LEITURA (Para o Revisor/Reviewer)

**Olá, Revisor! Ao revisar este PR, por favor, verifique os seguintes pontos:**

1.  **Objetivo do Commit:** Os commits são atômicos e a mensagem é clara e segue o padrão (Ex: `feat:`, `fix:`, `refactor:`)?
2.  **Lógica:** A solução proposta resolve o problema da Issue e não introduz novos efeitos colaterais (bugs)?
3.  **Testes:** Os testes unitários/de integração foram adicionados/atualizados? O PR deve ter [X]% de cobertura.
4.  **Estilo/Padrões:** O código segue os padrões de estilo do projeto (linter)? (Ex: Nomenclatura, espaçamento, complexidade de função)
5.  **Performance:** Existem *queries* de banco de dados ou loops que podem degradar a performance?

**Se todos os pontos estiverem OK, use o `Approve` para liberar o Merge. Caso contrário, use `Request Changes` e seja específico nos comentários.**

---

## Checklist (Para Quem Criou o PR)

* [ ] Eu li e segui a [Prática de Leitura do Time](#-prática-de-leitura-para-o-revisorreviewer).
* [ ] Meu código não introduz *warnings* no console.
* [ ] Eu testei localmente e confirmei que a feature/bugfix funciona.
* [ ] Se for uma Feature, eu atualizei a documentação relevante.
* [ ] Eu adicionei um screenshot/vídeo se a mudança tiver impacto visual.
