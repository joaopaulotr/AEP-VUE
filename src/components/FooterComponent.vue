<template>
  <footer class="footer-custom">
    <div class="container">
      <div class="row g-4">
        <!-- Informações da plataforma -->
        <div class="col-lg-4 col-md-6">
          <div class="mb-4">
            <h5 class="fw-bold text-white mb-3">
              <i class="fas fa-city me-2"></i>
              Denúncias Urbanas
            </h5>
            <p class="text-light opacity-75 mb-4">
              Conectando cidadãos e prefeituras através da tecnologia para 
              construir cidades mais inteligentes e organizadas.
            </p>
            <div class="d-flex gap-3">
              <a href="#" class="text-light hover-lift" style="font-size: 1.5rem;">
                <i class="fab fa-facebook-f"></i>
              </a>
              <a href="#" class="text-light hover-lift" style="font-size: 1.5rem;">
                <i class="fab fa-twitter"></i>
              </a>
              <a href="#" class="text-light hover-lift" style="font-size: 1.5rem;">
                <i class="fab fa-instagram"></i>
              </a>
              <a href="#" class="text-light hover-lift" style="font-size: 1.5rem;">
                <i class="fab fa-linkedin-in"></i>
              </a>
              <a href="#" class="text-light hover-lift" style="font-size: 1.5rem;">
                <i class="fab fa-youtube"></i>
              </a>
            </div>
          </div>
        </div>

        <!-- Links úteis -->
        <div class="col-lg-2 col-md-6">
          <h6 class="fw-bold text-white mb-3">Links Úteis</h6>
          <ul class="list-unstyled">
            <li class="mb-2">
              <a href="#inicio" class="text-light opacity-75 text-decoration-none hover-link">
                Início
              </a>
            </li>
            <li class="mb-2">
              <a href="#objetivo" class="text-light opacity-75 text-decoration-none hover-link">
                Objetivo
              </a>
            </li>
            <li class="mb-2">
              <a href="#metodologia" class="text-light opacity-75 text-decoration-none hover-link">
                Metodologia
              </a>
            </li>
            <li class="mb-2">
              <a href="#resultados" class="text-light opacity-75 text-decoration-none hover-link">
                Resultados
              </a>
            </li>
            <li class="mb-2">
              <a href="#denuncia" class="text-light opacity-75 text-decoration-none hover-link">
                Fazer Denúncia
              </a>
            </li>
          </ul>
        </div>

        <!-- Contato -->
        <div class="col-lg-3 col-md-6">
          <h6 class="fw-bold text-white mb-3">Contato</h6>
          <ul class="list-unstyled">
            <li class="mb-2 d-flex align-items-center">
              <i class="fas fa-envelope me-2 text-primary-custom"></i>
              <span class="text-light opacity-75">contato@denunciasurbanas.com</span>
            </li>
            <li class="mb-2 d-flex align-items-center">
              <i class="fas fa-phone me-2 text-primary-custom"></i>
              <span class="text-light opacity-75">(11) 9999-9999</span>
            </li>
            <li class="mb-2 d-flex align-items-center">
              <i class="fas fa-map-marker-alt me-2 text-primary-custom"></i>
              <span class="text-light opacity-75">São Paulo, SP - Brasil</span>
            </li>
            <li class="mb-2 d-flex align-items-center">
              <i class="fas fa-clock me-2 text-primary-custom"></i>
              <span class="text-light opacity-75">24/7 Disponível</span>
            </li>
          </ul>
        </div>

        <!-- Newsletter -->
        <div class="col-lg-3 col-md-6">
          <h6 class="fw-bold text-white mb-3">Newsletter</h6>
          <p class="text-light opacity-75 mb-3">
            Receba atualizações sobre melhorias na plataforma e dicas de cidadania.
          </p>
          <div class="input-group mb-3">
            <input 
              type="email" 
              class="form-control" 
              placeholder="Seu e-mail"
              v-model="newsletterEmail"
            >
            <button 
              class="btn btn-primary-custom" 
              type="button"
              @click="subscribeNewsletter"
            >
              <i class="fas fa-paper-plane"></i>
            </button>
          </div>
          <small class="text-light opacity-50">
            Não enviamos spam. Seus dados estão seguros.
          </small>
        </div>
      </div>

      <!-- Linha divisória -->
      <hr class="my-4 border-light opacity-25">

      <!-- Copyright e créditos -->
      <div class="row align-items-center">
        <div class="col-md-6">
          <p class="text-light opacity-75 mb-0">
            © {{ currentYear }} Denúncias Urbanas. Todos os direitos reservados.
          </p>
        </div>
        <div class="col-md-6 text-md-end">
          <p class="text-light opacity-75 mb-0">
            Desenvolvido com 
            <i class="fas fa-heart text-danger mx-1"></i>
            para um futuro melhor
          </p>
        </div>
      </div>

      <!-- Tecnologias utilizadas -->
      <div class="row mt-3">
        <div class="col-12 text-center">
          <small class="text-light opacity-50">
            Desenvolvido com Vue.js, Bootstrap e EmailJS
          </small>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent',
  data() {
    return {
      newsletterEmail: '',
      currentYear: new Date().getFullYear()
    }
  },
  methods: {
    subscribeNewsletter() {
      if (this.newsletterEmail) {
        // Aqui você pode implementar a lógica de inscrição na newsletter
        alert('Obrigado por se inscrever! Em breve você receberá nossas atualizações.');
        this.newsletterEmail = '';
      } else {
        alert('Por favor, insira um e-mail válido.');
      }
    }
  }
}
</script>

<style scoped>
.footer-custom {
  background: linear-gradient(135deg, var(--dark-gray), #111827);
  color: white;
}

.hover-lift {
  transition: all 0.3s ease;
}

.hover-lift:hover {
  transform: translateY(-3px);
  color: var(--primary-blue) !important;
}

.hover-link {
  transition: all 0.3s ease;
}

.hover-link:hover {
  color: var(--primary-blue) !important;
  opacity: 1 !important;
  padding-left: 5px;
}

.btn-primary-custom {
  background: linear-gradient(135deg, var(--primary-blue), var(--accent-blue));
  border: none;
  transition: all 0.3s ease;
}

.btn-primary-custom:hover {
  background: linear-gradient(135deg, var(--accent-blue), var(--primary-blue));
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(37, 99, 235, 0.3);
}

.form-control {
  border: 2px solid rgba(255, 255, 255, 0.1);
  background-color: rgba(255, 255, 255, 0.1);
  color: white;
}

.form-control:focus {
  border-color: var(--primary-blue);
  background-color: rgba(255, 255, 255, 0.15);
  color: white;
  box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
}

.form-control::placeholder {
  color: rgba(255, 255, 255, 0.6);
}

.text-primary-custom {
  color: var(--accent-blue) !important;
}

@media (max-width: 768px) {
  .col-md-6 {
    text-align: center !important;
    margin-bottom: 1rem;
  }
  
  .text-md-end {
    text-align: center !important;
  }
}
</style>

