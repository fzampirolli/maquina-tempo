# Páginas públicas — Máquina do Tempo

Páginas públicas e estáticas do projeto Máquina do Tempo (CS2, Python, Moodle +
VPL, UFABC).

## Revisores e outras IES: implantar em um PC local

`https://fzampirolli.github.io/maquina-tempo/implantar.html`

Página com o pacote de revisão, requisitos de hardware e restrições web. O
pacote é autocontido e não contém token, dados de alunos nem acesso à rede
interna da UFABC.

- Release: `https://github.com/fzampirolli/maquina-tempo/releases/tag/v0.1-revisao-2026-11-14`
- Pacote: `maquina-tempo-review-2026-11-14.tar.gz`
- Portal demo local: `/tutor/professor`, token `demo-token`; turmas em `/tutor/professor/turmas`
- Sem GPU: timeline, casos, fluxograma e FAQ lexical.
- Com GPU: chat com o tutor, busca semântica e RAG de autoria.
- A instância da UFABC atende ao piloto de 2027 e **não** é oferecida como
  serviço hospedado; cada instituição instala a sua.

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

## Portal do professor

`https://vision.ufabc.edu.br/tutor/professor`

O professor entra com usuário e senha no portal, cria ou clona EPs, edita
enunciado, código, casos de teste, FAQ e visibilidade, e recebe os links/HTML
para o VPL. O antigo `/estudio/` redireciona para o portal.

## Serviço do aluno

- Aluno: `https://vision.ufabc.edu.br/tutor/aluno?atividade=cs2-ep04-10-triangulo`
- Timeline: `https://vision.ufabc.edu.br/tutor/maquina-tempo?atividade=cs2-ep04-10-triangulo`
- Consentimento: `https://vision.ufabc.edu.br/tutor/consentimento`
- Saúde: `https://vision.ufabc.edu.br/tutor/api/health`

A timeline Pyodide roda no navegador; o chat usa o `qwen3:14b` no `guiou-Dell`
pelo proxy/túnel do `vision`. O piloto ainda **não tem LTI/SSO**: a página é
aberta, com fila, cota e filtro de código; o chat exige o aceite do termo de
consentimento. A interface tem botão **EN/PT**.

## Código do projeto

O código completo (proxy, tracer, serviço, artigo e análise) fica no repositório
privado `fzampirolli/maquina-tempo-cs2`. O pacote público de revisão é gerado a
partir dele e publicado nas releases deste repositório.
