# Denúncias Urbanas - Plataforma de Denúncias Cidadãs

Uma aplicação Vue.js moderna e responsiva para facilitar a comunicação entre cidadãos e prefeituras na resolução de problemas urbanos.

## 🚀 Características

- **Interface Moderna**: Design responsivo com cores modernas e animações suaves
- **Formulário Completo**: Validação em tempo real e upload de imagens
- **Geolocalização**: Detecção automática da localização do usuário
- **E-mail Automático**: Sistema de confirmação via EmailJS
- **Responsivo**: Compatível com desktop, tablet e mobile
- **Acessível**: Seguindo boas práticas de acessibilidade

## 🛠️ Tecnologias Utilizadas

- **Vue.js 3** - Framework JavaScript reativo
- **Bootstrap 5** - Framework CSS responsivo
- **Font Awesome** - Ícones modernos
- **EmailJS** - Serviço de envio de e-mails
- **Vite** - Build tool moderna e rápida

## 📋 Funcionalidades

### Seções do Site
1. **Header** - Navegação com smooth scroll
2. **Introdução** - Apresentação do problema urbano
3. **Objetivo** - Missão da plataforma
4. **Metodologia** - Tecnologias e funcionamento
5. **Resultados Esperados** - Impactos mensuráveis
6. **Formulário de Denúncia** - Interface principal
7. **Considerações Finais** - Visão de futuro
8. **Footer** - Links úteis e contato

### Formulário de Denúncia
- Nome completo (obrigatório)
- E-mail (obrigatório, com validação)
- Tipo de ocorrência (dropdown com opções)
- Localização (com botão de geolocalização)
- Descrição detalhada (mínimo 20 caracteres)
- Upload de imagem (drag & drop, máx. 5MB)

## 🚀 Como Executar

### Pré-requisitos
- Node.js 16+ 
- npm ou yarn

### Instalação
```bash
# Clone o repositório
git clone <url-do-repositorio>

# Entre no diretório
cd denuncias-urbanas

# Instale as dependências
npm install

# Execute em modo desenvolvimento
npm run dev

# Acesse http://localhost:3000
```

### Build para Produção
```bash
# Gerar build otimizado
npm run build

# Preview do build
npm run preview
```

## 📧 Configuração do E-mail

Para ativar o envio de e-mails em produção:

1. Consulte o arquivo `EMAILJS_CONFIG.md`
2. Configure sua conta no EmailJS
3. Substitua as credenciais no componente `FormularioDenunciaComponent.vue`

## 📱 Responsividade

O site foi desenvolvido com abordagem mobile-first e é totalmente responsivo:

- **Desktop**: Layout completo com sidebar
- **Tablet**: Layout adaptado com navegação colapsável
- **Mobile**: Interface otimizada para toque

## 🎨 Design System

### Cores Principais
- **Azul Primário**: #2563eb
- **Verde Primário**: #16a34a
- **Cinza**: #6b7280
- **Branco**: #ffffff

### Animações
- Fade in para elementos principais
- Slide in para cards laterais
- Hover effects em botões e cards
- Smooth scroll na navegação

## 📁 Estrutura do Projeto

```
src/
├── components/           # Componentes Vue
│   ├── HeaderComponent.vue
│   ├── IntroducaoComponent.vue
│   ├── ObjetivoComponent.vue
│   ├── MetodologiaComponent.vue
│   ├── ResultadosComponent.vue
│   ├── FormularioDenunciaComponent.vue
│   ├── ConsideracoesFinaisComponent.vue
│   └── FooterComponent.vue
├── assets/              # Arquivos estáticos
│   └── style.css       # Estilos customizados
├── App.vue             # Componente principal
└── main.js             # Ponto de entrada
```

## 🔧 Customização

### Cores
Edite as variáveis CSS em `src/assets/style.css`:

```css
:root {
  --primary-blue: #2563eb;
  --primary-green: #16a34a;
  --primary-gray: #6b7280;
  /* ... */
}
```

### Conteúdo
Cada seção está em um componente separado para facilitar a manutenção.

## 🚀 Deploy

### Netlify
1. Conecte seu repositório
2. Configure build command: `npm run build`
3. Configure publish directory: `dist`

### Vercel
1. Importe o projeto
2. Configure framework preset: `Vue.js`
3. Deploy automático

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📞 Suporte

Para dúvidas ou suporte:
- E-mail: contato@denunciasurbanas.com
- Issues: Use a aba Issues do GitHub

---

**Desenvolvido com ❤️ para um futuro melhor**

