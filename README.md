# Landing Page — Orçamento para Manutenção de Redutores (Projeto Original)

## Categoria
**Landing Page / Geração de Leads**

## Detalhes
Projeto focado em conversão direta para serviços de manutenção especializada de redutores industriais. Layout responsivo, visual profissional e linguagem direta para facilitar contato via WhatsApp e captura de leads pelo formulário modal.

## Objetivo Principal
Geração de leads e conversão direta via WhatsApp para serviços de manutenção de redutores, com ênfase em agilidade no atendimento e redução de paradas inesperadas nas operações dos clientes.

## Foco
- Agilidade na obtenção de orçamentos.  
- Minimização de paradas inesperadas por meio de manutenção preventiva e corretiva.  
- Destacar a experiência técnica e confiança da REDUMEC (prova social, garantias e benefícios claros).

## Tecnologias (Frontend)
- **HTML5** — Estrutura semântica e acessível.  
- **CSS3** — Design clean, responsivo e mobile-first (variáveis CSS para paleta institucional, utilitários e breakpoints).  
- **JavaScript (vanilla)** — Lógica do modal de formulário, submissão para WhatsApp (URL encoded), animações discretas de scroll/entrada (Intersection Observer) e tratamento de usabilidade mobile (fechar modal, bloquear scroll).

## Design & UX
- Visual clean, profissional e alinhado à identidade institucional (cores, tipografia e ícones).  
- CTA dominante com botão flutuante de WhatsApp e botão primário no hero (ambos chamam para conversão).  
- Modal de formulário como fallback para quem preferir enviar dados antes do contato no WhatsApp.  
- Prova social (depoimentos) e benefícios apresentados em blocos curtos — leitura rápida para decisores.  
- Acessibilidade básica: `aria-labels` em botões, contraste suficiente e foco visível em formulários.  
- Experiência mobile otimizada: botões full-width, espaçamento para toque e imagens dimensionadas para mobile.

## Otimização
- Favicon e meta tags essenciais (viewport, theme-color, description).  
- Imagens otimizadas (WebP quando possível) e `loading="lazy"` nas imagens secundárias.  
- CSS modular com variáveis e breakpoints; evitar bibliotecas pesadas para reduzir payload.  
- Uso de links diretos para WhatsApp com `encodeURIComponent` para preservar texto do formulário.  
- Minimização de arquivos e uso de caching headers ao publicar.

## Estratégia de Deploy (sugestão)
- **Amazon S3**: hospedagem estática dos arquivos (HTML/CSS/JS/Assets).  
- **Amazon CloudFront**: CDN para baixa latência, compressão e cache global.  
- **AWS Certificate Manager (ACM)**: SSL/TLS gerenciado para HTTPS no CloudFront.  
- **DNS**: apontar domínio via CNAME/ALIAS para CloudFront; usar provedor DNS com suporte a TTL baixo para deploys rápidos.   
- **Observabilidade**: ativar logs de acesso no CloudFront e monitoramento básico (CloudWatch) para acompanhar tráfego e erros.

## Extras
- Pixel de rastreamento (Google Analytics 4 / Meta Pixel) para medir conversões e otimizar campanhas.  
- Testes A/B simples em CTA (texto/posição) para aumentar taxa de conversão.  
- Mensagem automática/roteiro curto no WhatsApp para qualificar leads rapidamente.

---
