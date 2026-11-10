# Testador de acesso ao Ollama — Máquina do Tempo

Página pública e estática para testar o acesso ao proxy do Ollama usado nos
laboratórios de CS2 (Python, Moodle + VPL) da UFABC.

- Abra `https://fzampirolli.github.io/maquina-tempo/`.
- Preencha a URL do proxy (por exemplo, `https://vision.ufabc.edu.br/ollama`),
  o tipo de API (`Ollama — POST /api/chat`), o modelo (`qwen3:14b`) e o token.
- Clique em **Testar conexão (GET)** e **Enviar prompt (POST)**.

A página não contém token, senha, chave SSH nem IP interno. O token é digitado
pelo usuário no próprio navegador e não é salvo.

O código completo do projeto (proxy, tracer, propostas e análise) fica no
repositório privado `fzampirolli/maquina-tempo-cs2`.
