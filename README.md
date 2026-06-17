# Sô Antônio Cafés Especiais — Site Institucional

Site institucional da **Sô Antônio Cafés Especiais**, café especial de altitude da Serra da Mantiqueira (Minas Gerais, Brasil) — uma marca da família Fortes Bustamante, desde 1952.

Página única (one-page) com seções de **História**, **Fazendas**, **Da fazenda à xícara**, **Premiações** (com certificados), vídeos e **Contato**.

🛒 **CTA "Compre online"** — botão de destaque (cabeçalho fixo, hero e menu mobile) que leva à loja: `https://soantonio.lojavirtualnuvem.com.br/`.

✉️ **Formulário de contato funcional** — envia as mensagens por e-mail via **Web3Forms** (sem necessidade de servidor próprio). Veja a configuração da chave abaixo.

🔖 **Favicon** — ícone social da marca (Sô Antônio) exibido na aba do navegador.

✅ **Totalmente responsivo** — adapta-se a desktop, tablet e celular (menu hambúrguer no mobile, grids que se reorganizam em uma coluna, tipografia e espaçamentos fluidos).

🌐 **Multilíngue** — seletor de idioma com bandeiras no cabeçalho: **Português 🇧🇷 · English 🇺🇸 · Español 🇪🇸 · 简体中文 🇨🇳**. A troca é instantânea (sem recarregar a página). As bandeiras são carregadas de `flagcdn.com` (requer internet).

---

## 🗂 Estrutura do repositório

```
.
├── index.html                  # Página pronta para deploy (entrada do site)
├── Site Institucional.dc.html  # Arquivo-fonte editável (Design Component)
├── support.js                  # Runtime que renderiza a página
├── assets/
│   ├── logos/                  # Logotipos (horizontal/vertical, azul/creme)
│   ├── selo/                   # Selo "Desde 1952"
│   ├── social/                 # Ícone social / favicon
│   ├── icons/                  # Ícones de café da marca
│   ├── illustrations/          # Ilustração da fazenda (Mantiqueira)
│   └── fotos/                  # Fotografias do site
│       └── premios/            # Certificados das premiações + selo Certifica Minas
├── .nojekyll                   # Necessário para o GitHub Pages servir as pastas
├── .gitignore
└── README.md
```

> O `index.html` é uma cópia pronta-para-publicar de `Site Institucional.dc.html`.
> Para **editar**, altere o `.dc.html` e copie o conteúdo para `index.html` antes de publicar
> (ou simplesmente edite ambos — o conteúdo é idêntico).

---

## ⚙️ Configuração — formulário de contato (Web3Forms)

O formulário envia as mensagens através do serviço gratuito **[Web3Forms](https://web3forms.com)**, que repassa cada envio para um e-mail. A chave de acesso (Access Key) já está configurada no arquivo, vinculada a **contato@soantonio.com.br**.

Para trocar a chave ou o e-mail de destino:

1. Gere uma nova Access Key gratuita em [web3forms.com](https://web3forms.com) informando o e-mail de destino.
2. No `index.html` (e no `Site Institucional.dc.html`), localize a linha:
   ```js
   WEB3FORMS_KEY = 'ba026a0d-f6a6-4358-916c-f0fe83ea783e';
   ```
   e substitua pelo seu código.

> O envio exige conexão com a internet (a requisição vai para `api.web3forms.com`).
> Recomenda-se fazer um envio de teste após o deploy para confirmar o recebimento.

---

## ▶️ Rodar localmente

O site precisa ser servido por HTTP (não basta abrir o arquivo direto, por causa do
carregamento de scripts). Use qualquer servidor estático:

```bash
# Python 3
python3 -m http.server 8000

# ou Node (npx)
npx serve .
```

Depois acesse **http://localhost:8000**.

> Os vídeos do YouTube e as fontes (Google Fonts) e a biblioteca de render (React via CDN)
> exigem conexão com a internet.

---

## 🚀 Deploy

### Opção 1 — GitHub Pages (recomendado, grátis)

1. Faça o push deste repositório para o GitHub.
2. No repositório, vá em **Settings → Pages**.
3. Em **Build and deployment → Source**, selecione **Deploy from a branch**.
4. Escolha a branch `main` e a pasta `/ (root)`. Salve.
5. Em alguns minutos o site estará no ar em
   `https://<seu-usuario>.github.io/<nome-do-repo>/`.

> O arquivo `.nojekyll` já está incluído para garantir que o GitHub Pages sirva
> corretamente todos os arquivos e pastas.

### Opção 2 — Netlify

1. Acesse [app.netlify.com](https://app.netlify.com) → **Add new site → Import an existing project**.
2. Conecte o repositório do GitHub.
3. **Build command:** _(deixe em branco)_ · **Publish directory:** `.`
4. Deploy.

### Opção 3 — Vercel

1. Acesse [vercel.com/new](https://vercel.com/new) e importe o repositório.
2. **Framework Preset:** _Other_ · **Output Directory:** `.`
3. Deploy.

---

## 🔧 Domínio personalizado

Para usar **soantonio.com.br**:

- **GitHub Pages:** Settings → Pages → Custom domain → `soantonio.com.br`, e crie
  um registro DNS `CNAME`/`A` apontando para o GitHub Pages no seu provedor de domínio.
- **Netlify/Vercel:** adicione o domínio nas configurações do projeto e siga as
  instruções de DNS exibidas.

---

## 📐 Identidade visual

O site segue o **Sistema de Design Sô Antônio**:

- **Cores:** Azul `#3D4B58`, Creme `#F1E9D3`, Papel `#F4EFE6`, Caramelo `#AB7D2C`, Marrom `#6F4E37`.
- **Tipografia:** *Noto Serif* (títulos) + *Figtree* (texto), via Google Fonts.
- **Elementos:** moldura marrom fina (estilo selo), bandas em azul, ilustração da Mantiqueira.

---

## 📞 Contato

**Sô Antônio Cafés Especiais** · Fortes Bustamante Agronegócios
CNPJ 65.522.636/0001-49 · Pedralva / MG · Serra da Mantiqueira
WhatsApp (35) 9.9152-2869 · contato@soantonio.com.br

© 2026 Sô Antônio Cafés Especiais. Todos os direitos reservados.
