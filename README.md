# Páginas públicas — Máquina do Tempo

Páginas públicas e estáticas do projeto Máquina do Tempo (CS2, Python, Moodle +
VPL, UFABC).

## Testador de acesso ao Ollama

`https://fzampirolli.github.io/maquina-tempo/`

Ferramenta do professor para testar o acesso ao proxy do Ollama usado nos
laboratórios.

- A URL do proxy já vem preenchida (sem barra no fim); ajuste se necessário.
  Escolha o tipo de API (`Ollama — POST /api/chat`), o modelo e informe o
  **token pessoal do professor**.
- Clique em **Testar conexão (GET)** para listar os modelos e escolha um cartão;
  depois clique em **Enviar prompt (POST)**.

O token é pessoal, não é salvo e não deve ser compartilhado com alunos. A versão
do aluno usa o token de serviço no servidor. A página não contém token, senha,
chave SSH nem IP interno.

## Estúdio de Atividades

`https://fzampirolli.github.io/maquina-tempo/estudio.html`

Prévia do estúdio do professor: escolher o estilo do tutor e os limites, ver o
prompt gerado, o cartão da atividade e a prévia do aluno. Os 6 capítulos
(sequencial, funções, condicional, laço, vetor e matriz) trazem cada um o seu
próprio código de exemplo, timeline e previsão.

O estúdio também está publicado no `vision`, em
`https://vision.ufabc.edu.br/estudio/`.

## Serviço do aluno no vision

- Aluno: `https://vision.ufabc.edu.br/tutor/aluno?atividade=cs2-ep4-10-triangulo`
- Saúde: `https://vision.ufabc.edu.br/tutor/api/health`

O serviço guarda o prompt e o token no servidor e chama o `qwen3:14b` no
`guiou-Dell` pelo proxy/túnel do `vision`. O piloto ainda **não tem LTI/SSO**:
a página é aberta, com fila, cota por IP e filtro de blocos de código. A
timeline Pyodide será integrada no próximo passo.

## Código do projeto

O código completo (proxy, tracer, propostas e análise) fica no repositório
privado `fzampirolli/maquina-tempo-cs2`.
