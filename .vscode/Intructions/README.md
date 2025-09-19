# Projeto: RID222165_Desafio02

Este documento contém configuração recomendada para formatação de código com Prettier e padrões de estilo para HTML, CSS e JavaScript puros (sem framework).

---

## 🎯 Objetivo

- Garantir código limpo, padronizado e legível.  
- Evitar estilos divergentes entre arquivos e colaboradores.  
- Automatizar formatação ao salvar ou via script.

---

## ⚙️ Instalação Prettier

Execute no diretório do projeto:

```bash
npm init -y
npm install --save-dev prettier
```

---

## 📁 Arquivos de configuração

### `.prettierrc`

```json
{
  "semi": true,
  "singleQuote": false,
  "tabWidth": 2,
  "trailingComma": "es5",
  "printWidth": 80,
  "useTabs": false,
  "bracketSpacing": true,
  "arrowParens": "always",
  "htmlWhitespaceSensitivity": "css",
  "endOfLine": "lf"
}
```

### `.prettierignore`

Use este arquivo para ignorar arquivos ou pastas que não precisam ser formatados:

```
node_modules/
dist/
build/
*.min.js
```

---

## 🔍 Explicação das opções

| Opção | Valor | Propósito |
|---|---|---|
| `semi` | `true` | Sempre usar ponto-e-vírgula no fim de instruções JS |
| `singleQuote` | `false` | Usar aspas duplas em strings |
| `tabWidth` | `2` | Indentação com dois espaços |
| `trailingComma` | `"es5"` | Vírgula final em objetos/arrays multilinha suportados pelo ES5 |
| `printWidth` | `80` | Limite de caracteres por linha para melhor leitura |
| `useTabs` | `false` | Utilizar espaços em vez de tabs para indentação |
| `bracketSpacing` | `true` | Espaços entre chaves `{ key: value }` |
| `arrowParens` | `"always"` | Parênteses sempre em arrow functions com um argumento |
| `htmlWhitespaceSensitivity` | `"css"` | Sensibilidade de espaços em arquivos HTML de acordo com as regras de CSS |
| `endOfLine` | `"lf"` | Usar quebra de linha tipo Unix para evitar inconsistências entre sistemas operacionais |

---

## 🚀 Script no `package.json`

Adicione no campo `"scripts"`:

```json
"scripts": {
  "format": "prettier --write \"**/*.{html,css,js}\""
}
```

Para formatar manualmente, rode:

```bash
npm run format
```

---

## 🛠️ Formatar automaticamente ao salvar (VS Code)

Se você usar o Visual Studio Code:

1. Instale a extensão **Prettier – Code Formatter**.  
2. No projeto, crie (se não existir) o arquivo `.vscode/settings.json` com:

   ```json
   {
     "editor.defaultFormatter": "esbenp.prettier-vscode",
     "editor.formatOnSave": true
   }
   ```

Assim, quando salvar HTML, CSS ou JS, a formatação será aplicada automaticamente.

---

## ✅ Checklist

- [ ] Prettier instalado localmente como dependência de desenvolvimento  
- [ ] `.prettierrc` configurado de acordo com este documento  
- [ ] `.prettierignore` ignorando pastas de build / arquivos irrelevantes  
- [ ] Script `"format"` no `package.json` funcionando  
- [ ] Editor configurado para formatar ao salvar  

---

Se quiser, incluo também instruções para lint de JS puro (sem framework), caso queira adicionar no futuro.
