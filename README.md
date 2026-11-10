# Testador de acesso ao Ollama — Máquina do Tempo

Página pública e estática para testar o acesso ao proxy do Ollama usado nos
laboratórios de CS2 (Python, Moodle + VPL) da UFABC.

- Abra `https://fzampirolli.github.io/maquina-tempo/`.
- A URL do proxy já vem preenchida (sem barra no fim); ajuste se necessário.
  Escolha o tipo de API (`Ollama — POST /api/chat`), o modelo e informe o **token pessoal do professor**.
- Clique em **Testar conexão (GET)** para listar os modelos e escolha um cartão;
  depois clique em **Enviar prompt (POST)**.

A página é uma **ferramenta do professor**. O token é pessoal, não é salvo e
não deve ser compartilhado com alunos. A versão do aluno usará LTI/SSO, com o
token de serviço no servidor. A página não contém token, senha, chave SSH nem
IP interno.

O código completo do projeto (proxy, tracer, propostas e análise) fica no
repositório privado `fzampirolli/maquina-tempo-cs2`.
