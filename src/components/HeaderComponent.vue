<template>
  <header class="header-custom">
    <nav class="navbar navbar-expand-lg navbar-dark">
      <div class="container">
        <!-- Logo e título -->
        <a class="navbar-brand d-flex align-items-center" href="#inicio">
          <div class="me-3">
            <i class="fas fa-city icon-large text-white"></i>
          </div>
          <div>
            <h3 class="mb-0 fw-bold">Denúncias Urbanas</h3>
            <small class="text-light opacity-75">Conectando Cidadão e Prefeitura</small>
          </div>
        </a>

        <!-- Botão toggle para mobile -->
        <button 
          class="navbar-toggler" 
          type="button" 
          data-bs-toggle="collapse" 
          data-bs-target="#navbarNav"
          aria-controls="navbarNav" 
          aria-expanded="false" 
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <!-- Menu de navegação -->
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <a class="nav-link fw-semibold" href="#inicio">Início</a>
            </li>
            <li class="nav-item">
              <a class="nav-link fw-semibold" href="#objetivo">Objetivo</a>
            </li>
            <li class="nav-item">
              <a class="nav-link fw-semibold" href="#metodologia">Metodologia</a>
            </li>
            <li class="nav-item">
              <a class="nav-link fw-semibold" href="#resultados">Resultados</a>
            </li>
            <li class="nav-item">
              <a class="nav-link fw-semibold" href="#denuncia">Fazer Denúncia</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
  mounted() {
    // Adicionar smooth scroll para os links de navegação
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({
            behavior: 'smooth',
            block: 'start'
          });
        }
      });
    });
  }
}
</script>

<style scoped>
.navbar-brand:hover {
  transform: scale(1.02);
  transition: transform 0.3s ease;
}

.nav-link {
  position: relative;
  transition: all 0.3s ease;
}

.nav-link:hover {
  color: #ffffff !important;
  transform: translateY(-2px);
}

.nav-link::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: 0;
  left: 50%;
  background-color: #ffffff;
  transition: all 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
  left: 0;
}

@media (max-width: 991px) {
  .navbar-nav {
    text-align: center;
    margin-top: 1rem;
  }
  
  .nav-link {
    padding: 0.75rem 0 !important;
  }
}
</style>

