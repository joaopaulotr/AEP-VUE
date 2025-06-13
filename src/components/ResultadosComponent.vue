<template>
  <section id="resultados" class="section-padding section-bg-light">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 mx-auto text-center mb-5 fade-in">
          <h2 class="display-5 fw-bold text-primary-custom mb-4">
            Resultados Esperados
          </h2>
          <p class="lead">
            Nossa plataforma visa gerar impactos positivos mensuráveis na qualidade 
            de vida urbana e na eficiência da gestão pública municipal.
          </p>
        </div>
      </div>

      <!-- Cards de Resultados -->
      <div class="row g-4 mb-5">
        <!-- Redução do Tempo de Resposta -->
        <div class="col-lg-6 slide-in-left">
          <div class="card card-custom h-100 p-4 hover-lift">
            <div class="row align-items-center">
              <div class="col-md-4 text-center">
                <div class="bg-gradient-primary rounded-circle d-inline-flex align-items-center justify-content-center mb-3" style="width: 100px; height: 100px;">
                  <i class="fas fa-tachometer-alt text-white" style="font-size: 2.5rem;"></i>
                </div>
              </div>
              <div class="col-md-8">
                <h4 class="fw-bold text-primary-custom mb-3">Redução do Tempo de Resposta</h4>
                <p class="text-muted mb-3">
                  Diminuição significativa no tempo entre a identificação do problema 
                  e o início das ações corretivas pela prefeitura.
                </p>
                <div class="d-flex align-items-center">
                  <div class="bg-success text-white px-3 py-1 rounded-pill fw-bold me-3">
                    -60%
                  </div>
                  <small class="text-muted">Tempo médio de resposta</small>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Aumento da Participação Cidadã -->
        <div class="col-lg-6 slide-in-right">
          <div class="card card-custom h-100 p-4 hover-lift">
            <div class="row align-items-center">
              <div class="col-md-4 text-center">
                <div class="bg-gradient-success rounded-circle d-inline-flex align-items-center justify-content-center mb-3" style="width: 100px; height: 100px;">
                  <i class="fas fa-users text-white" style="font-size: 2.5rem;"></i>
                </div>
              </div>
              <div class="col-md-8">
                <h4 class="fw-bold text-success-custom mb-3">Aumento da Participação Cidadã</h4>
                <p class="text-muted mb-3">
                  Maior engajamento dos cidadãos na melhoria da cidade através 
                  de uma plataforma acessível e fácil de usar.
                </p>
                <div class="d-flex align-items-center">
                  <div class="bg-primary text-white px-3 py-1 rounded-pill fw-bold me-3">
                    +150%
                  </div>
                  <small class="text-muted">Denúncias registradas</small>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Melhoria na Organização -->
        <div class="col-lg-6 fade-in" style="animation-delay: 0.2s;">
          <div class="card card-custom h-100 p-4 hover-lift">
            <div class="row align-items-center">
              <div class="col-md-4 text-center">
                <div class="bg-gradient-primary rounded-circle d-inline-flex align-items-center justify-content-center mb-3" style="width: 100px; height: 100px;">
                  <i class="fas fa-chart-line text-white" style="font-size: 2.5rem;"></i>
                </div>
              </div>
              <div class="col-md-8">
                <h4 class="fw-bold text-primary-custom mb-3">Melhoria na Organização</h4>
                <p class="text-muted mb-3">
                  Sistema organizado de priorização e acompanhamento de demandas 
                  urbanas pela gestão municipal.
                </p>
                <div class="d-flex align-items-center">
                  <div class="bg-warning text-dark px-3 py-1 rounded-pill fw-bold me-3">
                    +80%
                  </div>
                  <small class="text-muted">Eficiência operacional</small>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Transparência e Confiança -->
        <div class="col-lg-6 fade-in" style="animation-delay: 0.4s;">
          <div class="card card-custom h-100 p-4 hover-lift">
            <div class="row align-items-center">
              <div class="col-md-4 text-center">
                <div class="bg-gradient-success rounded-circle d-inline-flex align-items-center justify-content-center mb-3" style="width: 100px; height: 100px;">
                  <i class="fas fa-handshake text-white" style="font-size: 2.5rem;"></i>
                </div>
              </div>
              <div class="col-md-8">
                <h4 class="fw-bold text-success-custom mb-3">Transparência e Confiança</h4>
                <p class="text-muted mb-3">
                  Fortalecimento da relação entre cidadãos e governo através 
                  de comunicação clara e transparente.
                </p>
                <div class="d-flex align-items-center">
                  <div class="bg-info text-white px-3 py-1 rounded-pill fw-bold me-3">
                    +90%
                  </div>
                  <small class="text-muted">Satisfação dos usuários</small>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Métricas de Impacto -->
      <div class="row">
        <div class="col-12">
          <div class="card card-custom bg-gradient-primary text-white p-5">
            <h3 class="text-center fw-bold mb-5">Impacto Esperado na Cidade</h3>
            <div class="row g-4 text-center">
              <div class="col-lg-3 col-md-6">
                <div class="border-end border-light border-opacity-25 pe-4">
                  <h2 class="fw-bold mb-2">500+</h2>
                  <p class="mb-0 opacity-90">Denúncias por mês</p>
                </div>
              </div>
              <div class="col-lg-3 col-md-6">
                <div class="border-end border-light border-opacity-25 pe-4">
                  <h2 class="fw-bold mb-2">72h</h2>
                  <p class="mb-0 opacity-90">Tempo médio de resposta</p>
                </div>
              </div>
              <div class="col-lg-3 col-md-6">
                <div class="border-end border-light border-opacity-25 pe-4">
                  <h2 class="fw-bold mb-2">95%</h2>
                  <p class="mb-0 opacity-90">Taxa de resolução</p>
                </div>
              </div>
              <div class="col-lg-3 col-md-6">
                <h2 class="fw-bold mb-2">24/7</h2>
                <p class="mb-0 opacity-90">Disponibilidade</p>
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
  name: 'ResultadosComponent'
}
</script>

<style scoped>
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

.border-end {
  border-right: 1px solid rgba(255, 255, 255, 0.25) !important;
}

@media (max-width: 768px) {
  .display-5 {
    font-size: 2rem;
  }
  
  .border-end {
    border-right: none !important;
    border-bottom: 1px solid rgba(255, 255, 255, 0.25) !important;
    padding-bottom: 2rem !important;
    margin-bottom: 2rem !important;
  }
  
  .col-lg-3:last-child .border-end {
    border-bottom: none !important;
    margin-bottom: 0 !important;
    padding-bottom: 0 !important;
  }
}
</style>

