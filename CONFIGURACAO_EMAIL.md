# 📧 Configuração do EmailJS - GRATUITO

## 🚀 **Passo a Passo para Configurar o EmailJS**

### **1. Criar Conta no EmailJS (Gratuito)**
1. Acesse: https://www.emailjs.com/
2. Clique em "Sign Up" (Cadastrar)
3. Use seu e-mail do Gmail, Outlook ou outro
4. Confirme o e-mail de verificação

### **2. Configurar Serviço de E-mail**
1. No dashboard, clique em "Add New Service"
2. Escolha seu provedor:
   - **Gmail** (Recomendado)
   - **Outlook/Hotmail**
   - **Yahoo**
   - Outros
3. Faça a conexão com sua conta
4. Anote o **SERVICE_ID** gerado

### **3. Criar Templates de E-mail**

#### **Template 1: Notificação de Contato**
```
Template ID: template_contato
Assunto: Nova mensagem do site - {{from_name}}

Conteúdo:
Olá {{to_name}},

Você recebeu uma nova mensagem através do site da Potencialize Consultoria:

📝 **Dados do Cliente:**
- Nome: {{from_name}}
- E-mail: {{from_email}}
- Empresa: {{empresa}}
- Telefone: {{telefone}}
- Newsletter: {{newsletter}}

💬 **Mensagem:**
{{message}}

📅 **Data/Hora:** {{data_envio}}
🔗 **Origem:** {{origem}}

---
Potencialize Consultoria
```

#### **Template 2: Confirmação para Cliente**
```
Template ID: template_confirmacao
Assunto: Recebemos sua mensagem - Potencialize Consultoria

Conteúdo:
Olá {{to_name}},

Obrigado por entrar em contato com a {{company_name}}!

✅ Recebemos sua mensagem com sucesso e nossa equipe analisará seu contato.
📞 Retornaremos em até 24 horas.

Se precisar de algo urgente, entre em contato:
📧 contato@potencialize.com
📱 (11) 99999-9999

Atenciosamente,
Equipe Potencialize Consultoria
```

#### **Template 3: Solicitação de Download**
```
Template ID: template_download
Assunto: Solicitação de Download - {{produto_solicitado}}

Conteúdo:
Nova solicitação de download recebida:

👤 **Cliente:**
- Nome: {{from_name}}
- E-mail: {{from_email}}
- Empresa: {{empresa}}

📦 **Produto:** {{produto_solicitado}}
📅 **Data:** {{data_solicitacao}}
🔗 **Origem:** {{origem}}

Envie o material solicitado para o e-mail do cliente.
```

#### **Template 4: Confirmação de Download**
```
Template ID: template_download_confirmacao
Assunto: Seu download será enviado em breve!

Conteúdo:
Olá {{to_name}},

Recebemos sua solicitação do material: **{{produto_nome}}**

📧 Enviaremos o download para este e-mail em até 2 horas.
💡 Caso não receba, verifique sua caixa de spam.

Obrigado pela confiança!

Atenciosamente,
{{company_name}}
```

### **4. Obter Chaves de API**
1. Vá em "Account" > "General"
2. Copie sua **PUBLIC KEY**
3. Anote os **Template IDs** criados

### **5. Configurar no Código**
Substitua no arquivo `index.html`:

```javascript
// Linha ~895
emailjs.init({
  publicKey: "SUA_PUBLIC_KEY_AQUI", // Cole sua Public Key
});

// Linha ~975
await emailjs.send(
  'service_pxk2s85',       // Seu Service ID
  'template_contato',      // ID do template de contato
  templateParams
);

// Linha ~1010
await emailjs.send(
  'service_pxk2s85',          // Mesmo Service ID
  'template_confirmacao',     // ID do template de confirmação
  templateParams
);
```

### **6. Testar o Sistema**
1. Abra sua landing page
2. Preencha o formulário de contato
3. Verifique se recebeu o e-mail
4. Teste também os downloads

### **7. Limites da Versão Gratuita**
- ✅ **200 e-mails por mês**
- ✅ Todos os recursos básicos
- ✅ Templates ilimitados
- ✅ Suporte por e-mail

### **8. Alternativas Gratuitas**

#### **Opção 2: Netlify Forms**
```html
<!-- Substitua o form por: -->
<form name="contact" method="POST" data-netlify="true">
  <input type="hidden" name="form-name" value="contact">
  <!-- seus campos aqui -->
</form>
```

#### **Opção 3: Formspree**
```html
<!-- Substitua o form por: -->
<form action="https://formspree.io/f/SEU_FORM_ID" method="POST">
  <!-- seus campos aqui -->
</form>
```

## 🔧 **Configuração Rápida (5 minutos)**

1. **Criar conta**: EmailJS.com
2. **Conectar Gmail**: Add New Service > Gmail
3. **Criar template**: Copy/paste dos templates acima
4. **Pegar chaves**: Public Key + Service ID
5. **Colar no código**: Substituir as variáveis
6. **Testar**: Enviar formulário

## 📞 **Suporte**

Se precisar de ajuda:
- 📧 Documentação: https://www.emailjs.com/docs/
- 💬 Support: support@emailjs.com
- 📱 Video tutorial: YouTube "EmailJS tutorial"

---

**Resultado Final:**
✅ E-mails automáticos quando alguém preencher o formulário
✅ Confirmação para o cliente
✅ Notificação para você
✅ Sistema profissional e gratuito
