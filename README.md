# 🚀 Protótipos SEBRAE

Coleção de protótipos interativos desenvolvidos para SEBRAE.

## 📂 Estrutura

```
prototipos/
├── index.html (página inicial com navegação)
├── caixa-reconhecimento-receitas/
│   ├── index.html
│   ├── guia-reconhecimento.html
│   └── relatorio-reconhecimento-receitas.html
└── consultorias-reconhecimento-receita/
    ├── index.html
    ├── caixa-detalhes-estorno-pacial-recibo.html
    ├── caixa-devolucoes-parcial.html
    ├── caixa-email-alerta-execucoes-parcial.html
    ├── caixa-relatorio-execucao-parcial.html
    ├── consultorias-aprovacao-fiscal-horas-execucao.html
    └── consultorias-lancamento-horas-consultor-relatorio.html
```

## 🌐 Publicação

Os protótipos são publicados automaticamente via **GitHub Pages** através de um workflow de CI/CD.

### Acessar os Protótipos

**URL:** https://wandersonml.github.io/prototipos

### Configuração no GitHub

Para que o GitHub Pages funcione corretamente:

1. Acesse: **Settings** > **Pages**
2. Em "Build and deployment", selecione:
   - **Source:** `Deploy from a branch`
   - **Branch:** `gh-pages` (será criada automaticamente após o primeiro deploy)
   - **Folder:** `/ (root)`

3. Salve as configurações

### Fluxo de Deploy

1. Você faz push para a branch `main`
2. O GitHub Actions dispara automaticamente
3. O workflow copia os protótipos para a pasta `public`
4. Os arquivos são publicados na branch `gh-pages`
5. GitHub Pages publica automaticamente em alguns minutos

## 🛠️ Desenvolvimento Local

Para visualizar os protótipos localmente:

```bash
# Opção 1: Python
python -m http.server 8000

# Opção 2: Node.js (npx)
npx http-server -p 8000

# Opção 3: Ruby
ruby -run -ehttpd . -p8000
```

Depois acesse: `http://localhost:8000`

## 📝 Adicionando Novos Protótipos

1. Crie um novo diretório com o nome do protótipo
2. Adicione os arquivos HTML dentro do diretório
3. Crie um `index.html` no diretório com navegação para os protótipos
4. Edite o `index.html` raiz para incluir o novo protótipo na lista principal
5. Faça push - o deploy acontecerá automaticamente!

## 🔄 CI/CD

- **GitLab CI:** `.gitlab-ci.yml` - para deploy em GitLab Pages
- **GitHub Actions:** `.github/workflows/deploy.yml` - para deploy em GitHub Pages

---

Desenvolvido com HTML, CSS e JavaScript puro | SEBRAE
