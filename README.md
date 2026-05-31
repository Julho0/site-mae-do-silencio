# 🕯️ Mãe do Silêncio — Sistema de Gestão

> Sistema interno de gestão para a fábrica de velas artesanais **Mãe do Silêncio**, desenvolvido como aplicação web single-page com autenticação, controle de estoque, pedidos e portal do cliente.

[![Deploy](https://img.shields.io/badge/Deploy-Cloudflare%20Pages-F38020?logo=cloudflare&logoColor=white)](https://site-mae-do-silencio.pages.dev)
[![Supabase](https://img.shields.io/badge/Backend-Supabase-3ECF8E?logo=supabase&logoColor=white)](https://supabase.com)
[![HTML](https://img.shields.io/badge/Frontend-HTML%20%2F%20CSS%20%2F%20JS-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/HTML)

---

## 📋 Funcionalidades

| Módulo | Descrição |
|---|---|
| 🔐 **Autenticação** | Login seguro via Supabase Auth (admin e portal cliente) |
| 📦 **Estoque** | Controle de velas por diâmetro, altura e cor com alertas de nível mínimo |
| 📝 **Pedidos** | Criação, edição, priorização e atualização de status de pedidos |
| 👥 **Clientes** | Cadastro e histórico de compras por cliente |
| 🏭 **Produção** | Painel de urgências com itens críticos e demanda por pedidos em aberto |
| 📊 **Dashboard** | Visão geral com alertas, próximas entregas e estoque crítico |
| 🛒 **Portal Cliente** | Interface para clientes consultarem pedidos e fazerem novos pedidos |

---

## 🛠️ Tecnologias

- **Frontend:** HTML5 + CSS3 + JavaScript (Vanilla, SPA)
- **Backend / Banco de Dados:** [Supabase](https://supabase.com) (PostgreSQL + Auth)
- **Ícones:** [Tabler Icons](https://tabler.io/icons)
- **Tipografia:** [Google Fonts](https://fonts.google.com) — Playfair Display + Lato
- **Hospedagem:** [Cloudflare Pages](https://pages.cloudflare.com)

---

## 🚀 Deploy

O site é hospedado automaticamente via **Cloudflare Pages**, conectado a este repositório.  
Qualquer push na branch `main` dispara um deploy automático.

🌐 **URL de produção:** `https://site-mae-do-silencio.pages.dev`

---

## 🔐 Segurança

> [!IMPORTANT]
> Este projeto utiliza a **Supabase Anon (publishable) Key** no frontend, que é o comportamento esperado e seguro para aplicações client-side.
>
> A segurança dos dados é garantida pelas **Row Level Security (RLS) policies** configuradas no Supabase — não pela chave em si.
>
> ✅ A chave exposta é pública por design (tipo `sb_publishable_*`)  
> ✅ Acesso aos dados é controlado por RLS no banco  
> ✅ Autenticação obrigatória para operações administrativas  

**Checklist de segurança:**
- [x] Sem senhas hardcoded no código
- [x] Sem chaves secretas ou service keys expostas
- [x] Autenticação via Supabase Auth (JWT)
- [x] Separação de roles: admin vs. cliente
- [x] RLS habilitado no Supabase para todas as tabelas sensíveis

---

## 📁 Estrutura

```
site-mae-do-silencio/
├── index.html      # Aplicação completa (SPA)
├── logo.png        # Logo da marca
├── icon.png        # Ícone da aba do navegador (favicon)
└── README.md       # Este arquivo
```

---

## 💡 Como rodar localmente

Não é necessário nenhum build — basta abrir o `index.html` em um servidor local:

```bash
# Com Python (já vem instalado na maioria dos sistemas)
python -m http.server 8080

# Ou com Node.js
npx serve .
```

Acesse em `http://localhost:8080`

---

## 👤 Autor

Desenvolvido por **Julio** para uso interno da Mãe do Silêncio — Velas Artesanais.

---

<p align="center">
  <em>Feito com 🕯️ e dedicação</em>
</p>
