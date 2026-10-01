# Modo de preservação de créditos para o Claude Code

Sabe quando você está no meio de um trabalho grande no Claude Code, o limite de uso acaba
e fica tudo pela metade? Você não sabe o que foi feito, o que faltou, nem por onde retomar.

Isto aqui é uma regra que você cola no seu `CLAUDE.md` global. A partir daí o Claude passa
a se comportar de três jeitos, conforme o crédito que ainda resta:

| Restante | O que o Claude faz |
|---|---|
| Mais de 10% | Trabalha normalmente |
| De 6% a 10% | Avisa que está acabando, evita tarefa pesada e pede sua autorização antes de começar algo médio ou grande |
| 5% ou menos | Entra no **modo de preservação**: não começa trabalho grande, não usa subagentes, para num ponto seguro e deixa um resumo pra você continuar depois |

O resumo de continuidade sempre traz: o que foi concluído, arquivos alterados, testes
executados, pendências e o próximo passo.

A reserva final só é usada se você escrever exatamente: `AUTORIZO USAR A RESERVA FINAL`.

## Como instalar (1 minuto)

No terminal do Mac ou do Linux:

```bash
mkdir -p ~/.claude && curl -fsSL https://raw.githubusercontent.com/Visionarxx/claude-modo-preservacao/main/modo-preservacao.md >> ~/.claude/CLAUDE.md
```

Pronto. Vale pra todas as sessões novas do Claude Code.

Prefere fazer na mão? Abra o arquivo [`modo-preservacao.md`](modo-preservacao.md), copie
tudo e cole no fim do seu `~/.claude/CLAUDE.md` (se o arquivo não existir, crie).

Rode o comando só uma vez. Se rodar de novo, a regra aparece duplicada no arquivo.

## Um aviso honesto

Isto é uma instrução de comportamento, não uma trava técnica. Na maioria das sessões o
Claude **não consegue ver** o seu percentual de uso. Por isso a regra tem uma parte de
segurança: quando ele não tem acesso ao número, ele não inventa, ele te pede pra olhar o
indicador de uso. Então o hábito que resolve de verdade é este: quando o indicador do app
mostrar que está acabando, diga isso pro Claude, e ele já sabe o que fazer.

## Licença

MIT. Use, adapte e compartilhe à vontade.
