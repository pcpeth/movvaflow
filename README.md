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
Aba **Assistente IA**: categorização automática no import do CSV (aprende regras com o que você confirma), alertas de gastos fora do padrão (locais, sem custo), resumo mensal, dicas para as metas e chat sobre seus gastos. Usa a API da Anthropic com **a sua chave**, guardada só no navegador de cada aparelho (nunca no Drive, nos backups ou neste repositório). A IA recebe descrições e valores, totais por categoria, metas e projeção; não recebe nomes de contas nem saldos.

## Privacidade
Os dados ficam no navegador (localStorage) e, se você ativar a sincronização, também no seu próprio Google Drive. Este repositório não contém dados financeiros. O Client ID do Google não é segredo, mas nunca publique backups `.json`. Faça backup (Configurações) com frequência: limpar os dados do navegador apaga tudo.

## Como usar online (opcional)
Ative o GitHub Pages em *Settings → Pages → Deploy from a branch → main / root*.
Os dados continuam locais em cada navegador/dispositivo.
