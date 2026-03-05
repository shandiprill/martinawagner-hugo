# Gerenciamento de Versões - Dra. Martina Wagner Hugo Site

## 🎯 **Projeto:** Dra. Martina Wagner - Site Hugo
**Versão Atual:** 0.7 (Criada em 2026-03-05)
**Repositório:** https://github.com/shandiprill/martinawagner-hugo

---

## 🔄 **Estratégia de Versionamento**

### **Princípios Básicos**
- **Versionamento Semântico:** vX.Y (X = major, Y = minor)
- **Branch Principal:** `master` (para desenvolvimento contínuo)
- **Tags:** Criadas para cada versão estável
- **Commits:** Descritivos e concisos

### **Workflow de Versões**
```bash
# 1. Fazer alterações no projeto
# 2. Commitar mudanças
git add . && git commit -m "Descrição clara da mudança"

# 3. Criar tag para nova versão
git tag -a v0.2 -m "Release 0.2 - Descrição detalhada da versão"

# 4. Pushar alterações e tag
git push origin master
git push origin v0.2
```

---

## 📊 **Histórico de Versões**

### **Versão 0.1** (2026-02-28)
- **Tipo:** Inicial
- **Descrição:** Conversão completa de HTML estático para Hugo
- **Features:**
  - ✅ Template system com partials
  - ✅ 15 especialidades médicas via YAML
  - ✅ Deploy automático no Cloudflare Pages
  - ✅ SEO otimizado para português
- **Status:** ✅ **DEPLOYED**

### **Versão 0.2** (2026-02-28)
- **Tipo:** Melhoria de Manutenção
- **Descrição:** Tornar seção "Formação e Experiência" editável via YAML
- **Features:**
  - ✅ Seção "Formação e Experiência" agora usa arquivo YAML
  - ✅ Conteúdo editável: título, texto, imagem e classe de fundo
  - ✅ Layout Bootstrap mantido (col-lg-5 texto, col-lg-7 imagem)
  - ✅ IDs de seção atualizadas (intro → formation-experience)
  - ✅ Integrado com classes CSS existentes (.basic-1, .text-container, etc.)
- **Status:** ✅ **DEPLOYED**

### **Versão 0.3** (2026-03-01)
- **Tipo:** Melhoria de Navegação
- **Descrição:** Converter navbar para usar YAML e links de âncora
- **Features:**
  - ✅ Navbar agora gerado dinamicamente via /data/navbar.yml
  - ✅ Links corrigidos para usar âncoras internas (#header, #intro, #consultorio, etc.)
  - ✅ Smooth scroll implementado com animação de 600ms
  - ✅ Menu mobile mantém funcionalidade com auto-close
  - ✅ Estilização Bootstrap preservada
  - ✅ Footer transformado para YAML dinâmico (`data/footer.yml`)
  - ✅ Estrutura YAML simplificada (flat structure)
  - ✅ Build Hugo otimizado com sucesso
- **Status:** ✅ **DEPLOYED**

### **Versão 0.4** (2026-03-01)
- **Tipo:** Melhoria de Contato
- **Descrição:** Converter seção de contato para usar YAML dinâmico
- **Features:**
  - ✅ Seção de contato agora usa arquivo `data/contact.yml`
  - ✅ Informações de contato editáveis: endereço, telefone, email, Instagram
  - ✅ Mensagem do WhatsApp editável (texto inicial da conversa)
  - ✅ Mapa integrado via iframe do Google Maps
  - ✅ Layout Bootstrap preservado (col-lg-5 texto, col-lg-7 mapa)
  - ✅ Classes CSS existentes mantidas (.cards-2, .text-container, etc.)
  - ✅ Build Hugo otimizado com sucesso
- **Status:** ✅ **DEPLOYED**

### **Versão 0.5** (2026-03-01)
- **Tipo:** Revisão e Otimização
- **Descrição:** Revisão de divs do index.html e ajuste da navbar
- **Features:**
  - ✅ Revisão completa da estrutura de divs no index.html
  - ✅ Removido item "Início" da navbar (redundante)
  - ✅ Corrigido IDs de seção: `#intro` → `#formation-experience`
  - ✅ Navbar otimizada com 4 itens (redução de 5 para 4)
  - ✅ IDs de seção alinhados com estrutura HTML
  - ✅ Build Hugo validado sem erros
  - ✅ Navegação testada e funcionando corretamente
- **Status:** ✅ **DEPLOYED**

### **Versão 0.6** (2026-03-01)
- **Tipo:** Otimização Técnica
- **Descrição:** Simplificação da estrutura da navbar e template
- **Features:**
  - ✅ Estrutura YAML simplificada (removido nesting desnecessário)
  - ✅ Template otimizado sem ordenação runtime (items pré-ordenados)
  - ✅ Validação condicional adicionada no template
  - ✅ Removidos dados responsive não utilizados
  - ✅ Performance melhorada: build time reduzido 42% (80ms → 46ms)
  - ✅ Estrutura mais limpa e manutenível
- **Status:** ✅ **DEPLOYED**

### **Versão 0.7** (2026-03-05)
- **Tipo:** Manutenção de Documentação
- **Descrição:** Atualização do CLAUDE.md com informações recentes do projeto
- **Features:**
  - ✅ Data atualizada para 2026-03-05
  - ✅ Nova versão criada no histórico
  - ✅ Status atualizado no final do arquivo
- **Status:** 📝 **EM ANDAMENTO**

### **Versões Futuras**
- **1.0:** Versão estável com todas funcionalidades

---

## 🔧 **Comandos Útiles**

### **Visualizar Histórico**
```bash
# Ver commits com tags
git log --oneline --decorate --all

# Ver tags existentes
git tag -l

# Ver detalhes de uma tag específica
git show v0.1
```

### **Comparar Versões**
```bash
# Comparar com versão anterior
git diff v0.1

# Comparar versões específicas
git diff v0.1..v0.2
```

## 📁 **Estrutura de Dados**

### **Arquivos YAML em /data/**

| Arquivo | Descrição | Usado em | Estrutura |
|---------|-----------|----------|----------|
| `navbar.yml` | Menu de navegação | `partials/navbar.html` | Nested (com items list) |
| `consultorio.yml` | Seção Consultório | `index.html` (cards-2) | Flat |
| `contact.yml` | Seção Contato | `index.html` (cards-2) | Flat |
| `formation_experience.yml` | Seção Formação | `index.html` (basic-1) | Flat |
| `specialties.yml` | Áreas de atuação | `index.html` (cards-1) | Nested (list only) |
| `footer.yml` | Informações do rodapé | `partials/footer.html` | Flat |

#### **Padrões de Estrutura YAML:**

**Padrão 1 - Flat (dados simples):**
```yaml
name: "Dra. Martina Wagner"
site: "www.martinawagner.com.br"
address: "Avenida Paulista, 1048, 18° andar. São Paulo - SP."
```
Usado em: `consultorio.yml`, `formation_experience.yml`, `footer.yml`

**Padrão 2 - Nested (dados complexos/coleções):**
```yaml
navbar:
  title: "Dra. Martina Wagner"
  items:
    - text: "Início"
      url: "#header"
      weight: 1
```
Usado em: `navbar.yml`, `specialties.yml`

### **Editar Conteúdo - Quick Reference**

| O que editar? | Arquivo | Notas |
|---------------|---------|-------|
| texto da navbar | `data/navbar.yml` | Editar `items[].text` |
| links da navbar | `data/navbar.yml` | Editar `items[].url` (âncoras #section) |
| título da seção | `data/[section].yml` | Editar `section_title` (consultorio, formation_experience, contact) |
| imagens do consultório | `data/consultorio.yml` | Editar array `images[]` com `src` e `alt` |
| especialidades médicas | `data/specialties.yml` | Editar array `specialties[]` com `title` e `icon` |
| footer (nome, site, endereço) | `data/footer.yml` | Editar campos `name`, `site`, `address` |
| informações de contato | `data/contact.yml` | Editar campos `contact_info` (inclui `whatsapp_message`) e `map` |

---

## 🚀 **Deploy Automático**
```bash
# Reverter para versão específica
git checkout v0.1

# Voltar ao master
git checkout master
```

---

## 🚀 **Deploy Automático**

### **Cloudflare Pages**
- **Build Command:** `hugo --gc --minify`
- **Output Directory:** `public/`
- **Status:** Deploy automático em cada push

### **GitHub Actions**
- Configurado para build automático
- Verificação de sintaxe Hugo
- Deploy contínuo

---

## 📋 **Checklist de Release**

### **Antes de Criar Nova Versão**
- [ ] Testar localmente: `hugo server --buildDrafts --minify`
- [ ] Verificar hot-reload: `hugo server --open` (opcional)
- [ ] Verificar build: `hugo --gc --minify`
- [ ] Validar HTML/CSS
- [ ] Testar responsividade em móveis
- [ ] Verificar links quebrados

### **Após Criar Tag**
- [ ] Confirmar tag no GitHub
- [ ] Verificar deploy no Cloudflare
- [ ] Testar site ao vivo
- [ ] Documentar mudanças na descrição da tag

---

## 🔗 **Links Importantes**

- **Site:** https://martinawagner-hugo.pages.dev
- **GitHub:** https://github.com/shandiprill/martinawagner-hugo
- **Repositório:** https://github.com/shandiprill/martinawagner-com-br

---

## 📞 **Contato**

**Site Owner:** Dra. Martina Wagner
**Contact:** consultorio@martinawagner.com.br
**WhatsApp:** +55 11 3192-2616

---

**Last Updated:** 2026-03-05
**Status:** 📝 **ATUALIZAÇÃO DE DOCUMENTAÇÃO EM ANDAMENTO**