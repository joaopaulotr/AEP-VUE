<template>
  <section id="metodologia" class="section-padding">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 mx-auto text-center mb-5 fade-in">
          <h2 class="display-5 fw-bold text-primary-custom mb-4">
            Metodologia e Tecnologias
          </h2>
          <p class="lead">
            Nossa plataforma utiliza tecnologias modernas e metodologias eficientes 
            para garantir uma experiência excepcional tanto para cidadãos quanto para gestores públicos.
          </p>
        </div>
      </div>

      <!-- Processo de Funcionamento -->
      <div class="row mb-5">
        <div class="col-12">
          <h3 class="text-center fw-bold mb-5 text-success-custom">Como Funciona</h3>
          <div class="row g-4">
            <!-- Passo 1 -->
            <div class="col-lg-3 col-md-6 text-center slide-in-left">
              <div class="position-relative mb-4">
                <div class="bg-gradient-primary rounded-circle d-inline-flex align-items-center justify-content-center" style="width: 100px; height: 100px;">
                  <span class="text-white fw-bold" style="font-size: 2rem;">1</span>
                </div>
                <div class="position-absolute top-50 start-100 translate-middle-y d-none d-lg-block" style="width: 50px; height: 2px; background: linear-gradient(90deg, var(--primary-blue), var(--primary-green));"></div>
              </div>
              <h5 class="fw-bold mb-3">Identificação</h5>
              <p class="text-muted">
                Cidadão identifica um problema urbano em sua região
              </p>
            </div>

            <!-- Passo 2 -->
            <div class="col-lg-3 col-md-6 text-center fade-in" style="animation-delay: 0.2s;">
              <div class="position-relative mb-4">
                <div class="bg-gradient-success rounded-circle d-inline-flex align-items-center justify-content-center" style="width: 100px; height: 100px;">
                  <span class="text-white fw-bold" style="font-size: 2rem;">2</span>
                </div>
                <div class="position-absolute top-50 start-100 translate-middle-y d-none d-lg-block" style="width: 50px; height: 2px; background: linear-gradient(90deg, var(--primary-green), var(--primary-blue));"></div>
              </div>
              <h5 class="fw-bold mb-3">Denúncia</h5>
              <p class="text-muted">
                Preenchimento do formulário com detalhes e fotos do problema
              </p>
            </div>

            <!-- Passo 3 -->
            <div class="col-lg-3 col-md-6 text-center fade-in" style="animation-delay: 0.4s;">
              <div class="position-relative mb-4">
                <div class="bg-gradient-primary rounded-circle d-inline-flex align-items-center justify-content-center" style="width: 100px; height: 100px;">
                  <span class="text-white fw-bold" style="font-size: 2rem;">3</span>
                </div>
                <div class="position-absolute top-50 start-100 translate-middle-y d-none d-lg-block" style="width: 50px; height: 2px; background: linear-gradient(90deg, var(--primary-blue), var(--primary-green));"></div>
              </div>
              <h5 class="fw-bold mb-3">Processamento</h5>
              <p class="text-muted">
                Prefeitura recebe e analisa a denúncia automaticamente
              </p>
            </div>

            <!-- Passo 4 -->
            <div class="col-lg-3 col-md-6 text-center slide-in-right">
              <div class="position-relative mb-4">
                <div class="bg-gradient-success rounded-circle d-inline-flex align-items-center justify-content-center" style="width: 100px; height: 100px;">
                  <span class="text-white fw-bold" style="font-size: 2rem;">4</span>
                </div>
              </div>
              <h5 class="fw-bold mb-3">Resolução</h5>
              <p class="text-muted">
                Ação é tomada e cidadão recebe confirmação por e-mail
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Tecnologias Utilizadas -->
      <div class="row">
        <div class="col-12">
          <h3 class="text-center fw-bold mb-5 text-primary-custom">Tecnologias Utilizadas</h3>
          <div class="row g-4">
            <!-- Vue.js -->
            <div class="col-lg-4 col-md-6">
              <div class="card card-custom h-100 p-4 hover-lift">
                <div class="text-center">
                  <i class="fab fa-vuejs icon-large text-success"></i>
                  <h5 class="fw-bold mt-3 mb-3">Vue.js</h5>
                  <p class="text-muted">
                    Framework JavaScript moderno para criação de interfaces reativas e componentes reutilizáveis.
                  </p>
                </div>
              </div>
            </div>

            <!-- Bootstrap -->
            <div class="col-lg-4 col-md-6">
              <div class="card card-custom h-100 p-4 hover-lift">
                <div class="text-center">
                  <i class="fab fa-bootstrap icon-large text-primary"></i>
                  <h5 class="fw-bold mt-3 mb-3">Bootstrap</h5>
                  <p class="text-muted">
                    Framework CSS para design responsivo e componentes prontos, garantindo compatibilidade mobile.
                  </p>
                </div>
              </div>
            </div>

            <!-- EmailJS -->
            <div class="col-lg-4 col-md-6">
              <div class="card card-custom h-100 p-4 hover-lift">
                <div class="text-center">
                  <i class="fas fa-envelope icon-large text-warning"></i>
                  <h5 class="fw-bold mt-3 mb-3">EmailJS</h5>
                  <p class="text-muted">
                    Serviço de envio de e-mails automático para confirmações e notificações aos usuários.
                  </p>
                </div>
              </div>
            </div>

            <!-- Geolocalização -->
            <div class="col-lg-4 col-md-6">
              <div class="card card-custom h-100 p-4 hover-lift">
                <div class="text-center">
                  <i class="fas fa-map-marker-alt icon-large text-danger"></i>
                  <h5 class="fw-bold mt-3 mb-3">Geolocalização</h5>
                  <p class="text-muted">
                    API de geolocalização para identificar automaticamente a localização dos problemas reportados.
                  </p>
                </div>
              </div>
            </div>

            <!-- Upload de Imagens -->
            <div class="col-lg-4 col-md-6">
              <div class="card card-custom h-100 p-4 hover-lift">
                <div class="text-center">
                  <i class="fas fa-camera icon-large text-info"></i>
                  <h5 class="fw-bold mt-3 mb-3">Upload de Imagens</h5>
                  <p class="text-muted">
                    Sistema de upload para anexar fotos dos problemas, facilitando a identificação e resolução.
                  </p>
                </div>
              </div>
            </div>

            <!-- Responsivo -->
            <div class="col-lg-4 col-md-6">
              <div class="card card-custom h-100 p-4 hover-lift">
                <div class="text-center">
                  <i class="fas fa-mobile-alt icon-large text-secondary"></i>
                  <h5 class="fw-bold mt-3 mb-3">Design Responsivo</h5>
                  <p class="text-muted">
                    Interface adaptável para todos os dispositivos: desktop, tablet e smartphone.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MetodologiaComponent'
}
</script>

<style scoped>
.icon-large {
  font-size: 3rem;
}

.bg-gradient-primary {
  background: linear-gradient(135deg, var(--primary-blue), var(--accent-blue));
}

.bg-gradient-success {
  background: linear-gradient(135deg, var(--primary-green), var(--accent-green));
}

.card {
  transition: all 0.3s ease;
  border: none;
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
}

/* Animações */
.fade-in {
  animation: fadeIn 0.8s ease-in;
}

.slide-in-left {
  animation: slideInLeft 0.8s ease-out;
}

.slide-in-right {
  animation: slideInRight 0.8s ease-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  from {
    opacity: 0;
    transform: translateX(50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@media (max-width: 768px) {
  .icon-large {
    font-size: 2rem;
  }
  
  .display-5 {
    font-size: 2rem;
  }
}
</style>

