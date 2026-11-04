# MovvaFlow – Finanças pessoais

App de finanças pessoais em **um único arquivo HTML** (sem servidor, sem instalação).
Abra `index.html` no navegador e use.

## Recursos
- Lançamentos, contas, cartões, receitas e empréstimos
- Projeção de caixa de 24 meses e rota para sair do vermelho
- Revisão de gastos e orçamento por categoria
- **Metas (v3.4):** reserva de emergência, juntar valor, quitar dívida, renda extra mensal e teto de gastos, com previsão de conclusão, aporte sugerido e análise de prazos
- Backup e restauração em JSON

## Sincronização entre aparelhos (v3.5)
Em *Configurações › Sincronização (Google Drive)*, conecte com o Client ID do Google. Os dados ficam num arquivo na pasta privada do app no seu Drive (escopo `drive.appdata`), sem passar por servidor de terceiros. Cada alteração sobe após ~3 s; ao abrir o app, o primeiro toque sincroniza. Se os dois aparelhos mudarem ao mesmo tempo, o app pede para escolher qual versão manter.

## Assistente IA (v3.6)
Botão flutuante 🤖 em todas as abas (v3.7): chat que entende a aba atual e propõe ações (lançar gasto por frase, criar/ajustar metas, recategorizar, abrir telas filtradas), sempre com confirmação. Aba **Assistente IA**: categorização automática no import do CSV (aprende regras com o que você confirma), alertas de gastos fora do padrão (locais, sem custo), resumo mensal, dicas para as metas e chat sobre seus gastos. Usa a API da Anthropic com **a sua chave**, guardada só no navegador de cada aparelho (nunca no Drive, nos backups ou neste repositório). A IA recebe descrições e valores, totais por categoria, metas e projeção; recebe os nomes das contas (para lançar na conta certa), mas saldos só se você ativar.

## Inteligência local (v3.8, sem custo e sem IA externa)
- **Aprende com o seu histórico:** ao importar CSV ou lançar, a categoria é sugerida pelo que você já classificou antes (estabelecimento e palavras), com nível de confiança. Corrigir uma categoria melhora as próximas sugestões.
- **Prioridades de hoje** no Painel, ordenadas por gravidade, e **Previsão do mês** por categoria.
- **Sugerir categorias** para lançamentos sem categoria (histórico primeiro, IA opcional).
- **Escreva como fala** ao criar um lançamento: "45 ifood ontem no cartão".
- Com a chave da IA, o assistente consulta os lançamentos com cálculos exatos em vez de estimar.

## Categorias (v3.9)
- **Conjunto sugerido (12 categorias enxutas):** soma ao que você já tem, reaproveitando nomes parecidos (sem duplicar), com prévia antes de aplicar.
- **Regras de palavras-chave** de estabelecimentos brasileiros (iFood, Uber, Drogasil, Netflix...). Suas regras continuam valendo e têm prioridade; a busca ignora acentos e maiúsculas.
- **Orçamento sugerido** pela média dos últimos meses +5%.
- **Gerenciador** em Configurações: renomear, mesclar e excluir (atualiza lançamentos, regras, orçamentos e metas), criar, ver média por mês e marcar "conta como gasto".

## Modo enxuto (v4.0)
Começo simples: só **Painel, Lançamentos e Metas** (mais Configurações) ficam ativos; as demais abas aparecem como "Em breve" e o assistente flutuante fica oculto. Lançamento pede só data, valor, descrição, conta e categoria (meio e tipo são automáticos). Nenhum dado é apagado; em Configurações › Modo do app dá para liberar todas as abas.

## Privacidade
Os dados ficam no navegador (localStorage) e, se você ativar a sincronização, também no seu próprio Google Drive. Este repositório não contém dados financeiros. O Client ID do Google não é segredo, mas nunca publique backups `.json`. Faça backup (Configurações) com frequência: limpar os dados do navegador apaga tudo.

## Como usar online (opcional)
Ative o GitHub Pages em *Settings → Pages → Deploy from a branch → main / root*.
Os dados continuam locais em cada navegador/dispositivo.
