# Gerenciamento de Versões - Dra. Martina Wagner Hugo Site

## 🎯 **Projeto:** Dra. Martina Wagner - Site Hugo
**Versão Atual:** 0.1 (Criada em 2026-02-28)
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

### **Versões Futuras**
- **0.2:** Atualizações de conteúdo e correções
- **0.3:** Melhorias técnicas e performance
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

### **Reverter Mudanças**
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

**Last Updated:** 2026-02-28
**Status:** ✅ **VERSÃO 0.1 CRIADA COM SUCESSO**