# 🚀 Gemini CLI Skills Collection

Uma coleção de skills personalizadas para o [Gemini CLI](https://github.com/google/gemini-cli), focada em produtividade e integração de ferramentas de IA.

## 🧠 Skills Disponíveis

### 1. Claude-Mem Integration
Permite que o Gemini CLI utilize a memória persistente do plugin `claude-mem` (do Claude Code). Ideal para manter a continuidade entre sessões e diferentes agentes de IA.

*   **Destaques:** Busca semântica no histórico, salvamento automático de descobertas e integração com o dashboard local (`localhost:37777`).
*   **Instalação:** 
    ```bash
    gemini skills install https://github.com/kaicmurilo/gemini-skill-claude-mem/raw/main/dist/claude-mem.skill --scope user
    ```

---

## 🛠️ Como Instalar as Skills

Você pode instalar qualquer skill desta coleção usando o comando `gemini skills install` apontando para o arquivo `.skill` na pasta `dist/`.

### Exemplo (Instalação Global):
```bash
gemini skills install dist/claude-mem.skill --scope user
```

### Após a Instalação:
Não esqueça de recarregar as skills na sua sessão ativa do Gemini CLI:
```bash
/skills reload
```

---

## 🏗️ Como Contribuir ou Usar o Código Fonte

Se você quiser modificar as skills ou entender como funcionam, os arquivos fonte estão na pasta `skills/`.

1. Clone o repositório:
   ```bash
   git clone https://github.com/kaicmurilo/gemini-skill-claude-mem.git
   ```
2. Explore o `SKILL.md` de cada pasta para ver as instruções do agente.

---
*Mantido por [@kaicmurilo](https://github.com/kaicmurilo)*
