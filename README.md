# 🧠 Gemini CLI Skill: Claude-Mem

Esta skill integra o [Gemini CLI](https://github.com/google/gemini-cli) com o plugin de memória persistente [claude-mem](https://github.com/thedotmack/claude-mem) (originalmente para Claude Code).

## 🚀 O que esta Skill faz?
Permite que o Gemini CLI acesse o histórico de sessões anteriores, decisões de arquitetura e observações salvas pelo Claude Code, mantendo a continuidade do trabalho entre diferentes agentes e sessões de IA.

- **Busca Semântica:** O Gemini pode pesquisar no seu histórico local.
- **Salvamento de Memórias:** O Gemini registra automaticamente novas descobertas na API do `claude-mem`.
- **Integração Visual:** Funciona em conjunto com o dashboard local (`http://localhost:37777`).

## 🛠️ Instalação

### Instalação via URL
Você pode instalar esta skill diretamente do GitHub:

```bash
gemini skills install https://github.com/kaicmurilo/gemini-skill-claude-mem/raw/main/dist/claude-mem.skill --scope user
```

### Instalação Local (se clonar o repo)
```bash
gemini skills install dist/claude-mem.skill --scope user
```

## 🔄 Após Instalar
Sempre que instalar ou atualizar uma skill, recarregue o agente no terminal:
```bash
/skills reload
```

---
*Mantido por [@kaicmurilo](https://github.com/kaicmurilo)*
