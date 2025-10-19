# Documentação Técnica - Landing Page REDUMEC

## 📖 Visão Geral

A landing page REDUMEC foi desenvolvida com foco em **conversão de leads** para o WhatsApp, utilizando um design clean, profissional e mobile-first. O projeto é totalmente responsivo, otimizado para performance e acessibilidade.

## 🏗️ Arquitetura

### Estrutura HTML
O arquivo `index.html` contém toda a estrutura semântica da página, organizada em seções:

1. **Header**: Navegação sticky com logo e CTA
2. **Hero Section**: Seção principal com headline e CTAs
3. **Problem Section**: Cards explicativos dos problemas
4. **Services Section**: Detalhamento dos serviços
5. **Benefits Section**: 6 benefícios principais
6. **Testimonials Section**: Depoimentos de clientes
7. **CTA Section**: Chamada final para ação
8. **Footer**: Informações de contato

### CSS Inline
Todo o CSS está inline no `<style>` do HTML para:
- Reduzir requisições HTTP
- Melhorar performance de carregamento
- Facilitar deploy em plataformas como Vercel

**Variáveis CSS (CSS Custom Properties)**:
```css
--primary-color: #0891b2        /* Azul ciano - cor principal */
--primary-dark: #0e7490         /* Azul escuro - hover/ativo */
--secondary-color: #1f2937      /* Cinza escuro - footer */
--light-bg: #f9fafb             /* Fundo claro */
--white: #ffffff                /* Branco */
--text-dark: #111827            /* Texto escuro */
--text-light: #6b7280           /* Texto claro */
--border-color: #e5e7eb         /* Bordas */
```

### JavaScript Vanilla
Funcionalidades implementadas sem dependências externas:

1. **Modal de Formulário**:
   - `openFormModal()`: Abre o modal
   - `closeFormModal()`: Fecha o modal
   - Suporta fechar clicando fora do modal

2. **Submissão de Formulário**:
   - Captura dados do formulário
   - Monta mensagem formatada para WhatsApp
   - Redireciona para o WhatsApp com mensagem pré-preenchida
   - Reseta o formulário após envio

3. **Navegação Suave**:
   - Scroll smooth para links de âncora
   - Detecta seções válidas antes de navegar

4. **Animações de Scroll**:
   - Intersection Observer para animar elementos ao entrar na viewport
   - Efeito fade-in para cards e benefícios

## 🎨 Design System

### Tipografia
```css
Font Stack: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif
```

**Tamanhos**:
- H1 (Hero): clamp(2rem, 5vw, 3.5rem) - responsivo
- H2 (Seções): 2.25rem
- H3 (Cards): 1.25rem
- Parágrafo: 1rem
- Small: 0.9rem

### Espaçamento
Utiliza sistema de 0.5rem (8px):
- Padding padrão: 1.5rem, 2rem, 2.5rem
- Gap entre elementos: 1rem, 1.5rem, 2rem
- Margin bottom: 1rem, 1.5rem, 2rem

### Sombras
```css
--shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05)
--shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1)
--shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1)
```

### Animações
- **Fade In**: Elementos aparecem com opacity
- **Slide Up**: Modal sobe com transform
- **Hover Effects**: Cards e botões se movem levemente
- **Transições**: 0.3s ease para suavidade

## 📱 Responsividade

### Breakpoints
```css
Desktop: 1200px+
Tablet: 768px - 1199px
Mobile: < 768px
```

### Ajustes por Device
- **Mobile**: Navegação reduzida, botões em coluna, modal centralizado
- **Tablet**: Layout intermediário com 2 colunas
- **Desktop**: Layout completo com 3+ colunas

## 🔗 Integração WhatsApp

### Formato da URL
```
https://wa.me/[CÓDIGO_PAÍS][NÚMERO]?text=[MENSAGEM_CODIFICADA]
```

### Exemplo
```
https://wa.me/5511999999999?text=Olá,%20gostaria%20de%20um%20orçamento...
```

### Fluxo de Conversão
1. Usuário clica em CTA do WhatsApp
2. Abre o WhatsApp com número pré-preenchido
3. Mensagem padrão aparece no campo de texto
4. Usuário pode enviar ou editar a mensagem

### Fluxo do Formulário
1. Usuário clica em "Preencher Formulário"
2. Modal abre com campos de entrada
3. Usuário preenche dados (Nome, E-mail, Telefone, Empresa, Mensagem)
4. Ao enviar, dados são incorporados na mensagem WhatsApp
5. Redireciona para WhatsApp com mensagem completa

## ⚡ Performance

### Otimizações Implementadas
1. **CSS Inline**: Elimina requisições externas
2. **JavaScript Vanilla**: Sem dependências pesadas
3. **Imagens Otimizadas**: Logo em PNG com compressão
4. **Lazy Loading**: Intersection Observer para animações
5. **Sem Fonts Externas**: Utiliza system fonts
6. **Minificação**: CSS e JS compactados

### Métricas Esperadas
- **Lighthouse Performance**: 95+
- **Lighthouse Accessibility**: 95+
- **Lighthouse Best Practices**: 95+
- **Lighthouse SEO**: 100
- **Time to Interactive**: < 1s
- **Cumulative Layout Shift**: 0

## 🔍 SEO

### Meta Tags
```html
<meta name="description" content="...">
<meta name="theme-color" content="#0891b2">
<title>REDUMEC - Manutenção de Redutores Industriais | Orçamento Grátis</title>
```

### Estrutura Semântica
- `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`
- Headings hierárquicos (H1, H2, H3)
- `<img>` com alt text descritivo
- Links com texto descritivo

### Open Graph (Recomendado adicionar)
```html
<meta property="og:title" content="REDUMEC - Manutenção de Redutores">
<meta property="og:description" content="...">
<meta property="og:image" content="...">
<meta property="og:url" content="...">
```

## ♿ Acessibilidade

### WCAG 2.1 Compliance
- ✅ Contraste de cores adequado (AA)
- ✅ Navegação por teclado funcional
- ✅ Semântica HTML correta
- ✅ Alt text em imagens
- ✅ Labels em formulários
- ✅ Focus states visíveis

### Melhorias Implementadas
- Botões com hover/focus states
- Inputs com focus ring
- Modal com close button acessível
- Scroll smooth em navegação

## 🔐 Segurança

### Práticas Implementadas
- ✅ Sem armazenamento de dados sensíveis
- ✅ Links WhatsApp seguros (wa.me)
- ✅ Validação HTML5 de formulário
- ✅ Sem scripts externos
- ✅ HTTPS recomendado para produção

### Dados do Formulário
- Não são armazenados no servidor
- Apenas redirecionam para WhatsApp
- Usuário controla o envio

## 📊 Analytics (Recomendado)

Para rastrear conversões, adicione:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>

<!-- Facebook Pixel -->
<img height="1" width="1" style="display:none" src="https://www.facebook.com/tr?id=PIXEL_ID&ev=PageView&noscript=1" />
```

## 🚀 Deploy

### Vercel
1. Conecte repositório GitHub
2. Configure branch `main`
3. Clique em Deploy
4. Domínio automático em `redumec.vercel.app`

### Customização de Domínio
1. Vá para Settings > Domains
2. Adicione seu domínio
3. Configure DNS records

## 🔧 Manutenção

### Atualizações Comuns

**Alterar número WhatsApp**:
```html
<!-- Procure por: 5511999999999 -->
<!-- Substitua por seu número -->
```

**Alterar logo**:
```html
<!-- Substitua assets/logo-redumec.png -->
```

**Editar textos**:
- Procure pelo texto na página
- Edite diretamente no HTML
- Commit e push para atualizar

**Adicionar nova seção**:
1. Crie um `<section>` com classe apropriada
2. Adicione CSS para a seção
3. Adicione JavaScript se necessário
4. Teste responsividade

## 📝 Changelog

### v1.0.0 (2025-10-19)
- ✨ Landing page inicial
- 🎨 Design clean e profissional
- 📱 Mobile-first responsivo
- 💬 Integração WhatsApp
- 📋 Formulário de fallback
- ⚡ Performance otimizada
- ♿ Acessibilidade WCAG 2.1

## 🤝 Suporte

Para dúvidas ou melhorias, abra uma issue no repositório GitHub.

---

**Última atualização**: 19 de Outubro de 2025

