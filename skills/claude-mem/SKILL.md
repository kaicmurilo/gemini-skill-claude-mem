---
name: claude-mem
description: Integração com o plugin de memória persistente claude-mem. Use para buscar históricos de sessões passadas do Claude Code e salvar novas descobertas para manter a continuidade entre diferentes agentes e sessões.
---

# Claude-Mem Integration

Este skill permite que o Gemini CLI utilize a base de conhecimento do plugin `claude-mem`.

## Quando usar
- Ao iniciar um projeto que já foi trabalhado com o Claude Code.
- Para recuperar decisões de arquitetura, bugs corrigidos ou progresso de tarefas anteriores.
- Para salvar "checkpoints" de memória que outros agentes poderão ler no futuro.

## Fluxo de Trabalho

### 1. Verificação de Saúde
Sempre verifique se o servidor local está rodando:
`curl -s http://localhost:37777/api/health`

### 2. Recuperação de Contexto (Research)
Ao iniciar uma tarefa, busque observações relevantes para o projeto atual:
`curl -s "http://localhost:37777/api/observations?project=<nome_projeto>&query=<termo_busca>"`

### 3. Registro de Memória (Finalização)
Ao concluir uma mudança significativa, salve o resumo:
`curl -X POST -H "Content-Type: application/json" -d '{"text": "<resumo>", "title": "<titulo>", "project": "<nome_projeto>"}' http://localhost:37777/api/memory/save`

## Dicas de Eficiência
- Use o parâmetro `limit` nas consultas para não sobrecarregar o contexto (ex: `limit=5`).
- Priorize os campos `facts` e `narrative` das observações retornadas.
- O nome do projeto (`project`) é essencial para filtrar resultados corretos.
