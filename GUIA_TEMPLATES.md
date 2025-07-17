# 🎯 GUIA RÁPIDO - Criar Templates EmailJS

## 📧 SEUS DADOS CONFIGURADOS
- **Service ID:** `service_gqvvapf` ✅
- **Public Key:** `z2336X6tKP2xg_f9D` ✅

## 🚀 CRIAR TEMPLATES (4 necessários)

### 📝 PASSO A PASSO:

1. **Acesse:** https://dashboard.emailjs.com/admin/templates
2. **Clique:** "Create New Template"
3. **Preencha os dados** conforme abaixo
4. **Salve** e **copie o Template ID**

---

## 📄 TEMPLATE 1: Contato Geral

**Template ID sugerido:** `template_contato`

**Subject:** Nova mensagem de contato - {{user_name}}

**Content:**
```
Olá!

Você recebeu uma nova mensagem de contato através do site:

Nome: {{user_name}}
Email: {{user_email}}
Telefone: {{telefone}}
Empresa: {{empresa}}
Newsletter: {{newsletter}}

Mensagem:
{{message}}

---
Enviado em: {{data_envio}}
Origem: {{origem}}
```

**Settings:**
- To Email: seu-email@dominio.com
- From Name: Site Consultoria
- Reply To: {{user_email}}

---

## ✅ TEMPLATE 2: Confirmação para Cliente

**Template ID sugerido:** `template_confirmacao`

**Subject:** Mensagem recebida com sucesso!

**Content:**
```
Olá {{user_name}},

Sua mensagem foi recebida com sucesso!

Retornaremos em breve através do email: {{user_email}}

Obrigado pelo contato!

---
Atenciosamente,
Equipe Potencialize Consultoria
```

**Settings:**
- To Email: {{user_email}}
- From Name: Potencialize Consultoria
- Reply To: seu-email@dominio.com

---

## 📥 TEMPLATE 3: Solicitação de Download

**Template ID sugerido:** `template_download`

**Subject:** Nova solicitação de download - {{produto}}

**Content:**
```
Nova solicitação de download!

Produto: {{produto}}
Nome: {{user_name}}
Email: {{user_email}}
Empresa: {{empresa}}

---
Enviado em: {{data_envio}}
```

**Settings:**
- To Email: seu-email@dominio.com
- From Name: Site Consultoria
- Reply To: {{user_email}}

---

## 📋 TEMPLATE 4: Confirmação de Download

**Template ID sugerido:** `template_download_confirmacao`

**Subject:** Download confirmado - {{produto}}

**Content:**
```
Olá {{user_name}},

Sua solicitação de download foi processada!

Produto: {{produto}}

Em breve você receberá o material no email: {{user_email}}

---
Atenciosamente,
Equipe Potencialize Consultoria
```

**Settings:**
- To Email: {{user_email}}
- From Name: Potencialize Consultoria
- Reply To: seu-email@dominio.com

---

## 📋 APÓS CRIAR OS TEMPLATES

**Me envie os 4 Template IDs:**
1. Template de Contato: `template_contato` (ou seu ID)
2. Template de Confirmação: `template_confirmacao` (ou seu ID)
3. Template de Download: `template_download` (ou seu ID)
4. Template Confirmação Download: `template_download_confirmacao` (ou seu ID)

## 🎯 ENTÃO PODEMOS:
- ✅ Atualizar o código com os Template IDs
- ✅ Testar o envio de emails reais
- ✅ Finalizar a configuração completa

---

💡 **DICA:** Use os IDs sugeridos para facilitar, ou me informe os IDs que você criar!
