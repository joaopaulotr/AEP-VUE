# Configuração do EmailJS para Produção

## Passos para configurar o EmailJS

### 1. Criar conta no EmailJS
1. Acesse [https://www.emailjs.com/](https://www.emailjs.com/)
2. Crie uma conta gratuita
3. Confirme seu e-mail

### 2. Configurar serviço de e-mail
1. No dashboard, vá em "Email Services"
2. Clique em "Add New Service"
3. Escolha seu provedor (Gmail, Outlook, etc.)
4. Configure as credenciais
5. Anote o **Service ID** gerado

### 3. Criar template de e-mail
1. Vá em "Email Templates"
2. Clique em "Create New Template"
3. Configure o template com as seguintes variáveis:
   - `{{from_name}}` - Nome do usuário
   - `{{from_email}}` - E-mail do usuário
   - `{{tipo_ocorrencia}}` - Tipo de problema reportado
   - `{{localizacao}}` - Localização do problema
   - `{{descricao}}` - Descrição detalhada
4. Anote o **Template ID** gerado

### 4. Obter chave pública
1. Vá em "Account" > "General"
2. Copie a **Public Key**

### 5. Atualizar o código
No arquivo `src/components/FormularioDenunciaComponent.vue`, substitua:

```javascript
await emailjs.send(
  'YOUR_SERVICE_ID',    // Substitua pelo seu Service ID
  'YOUR_TEMPLATE_ID',   // Substitua pelo seu Template ID
  templateParams,
  'YOUR_PUBLIC_KEY'     // Substitua pela sua Public Key
);
```

### 6. Remover comentários
Descomente o bloco de código do EmailJS e comente a simulação.

## Template de E-mail Sugerido

**Assunto:** Confirmação de Denúncia - Denúncias Urbanas

**Corpo:**
```
Olá {{from_name}},

Sua denúncia foi recebida com sucesso!

**Detalhes da Denúncia:**
- Tipo: {{tipo_ocorrencia}}
- Localização: {{localizacao}}
- Descrição: {{descricao}}

Nossa equipe analisará sua denúncia e tomará as medidas necessárias.

Obrigado por contribuir para uma cidade melhor!

Atenciosamente,
Equipe Denúncias Urbanas
```

## Limitações da Conta Gratuita
- 200 e-mails por mês
- Branding do EmailJS nos e-mails
- Suporte limitado

Para uso em produção, considere upgradar para um plano pago.

## Alternativas ao EmailJS
- **FormSubmit**: Serviço gratuito simples
- **Netlify Forms**: Para sites hospedados no Netlify
- **Backend próprio**: Usando Node.js + Nodemailer
- **Zapier**: Integração com diversos serviços

