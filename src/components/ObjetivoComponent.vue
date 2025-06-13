<template>
  <section id="objetivo" class="section-padding section-bg-light">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 mx-auto text-center mb-5 fade-in">
          <h2 class="display-5 fw-bold text-primary-custom mb-4">
            Nosso Objetivo
          </h2>
          <p class="lead">
            Fortalecer a comunicação entre cidadão e prefeitura através de uma plataforma 
            tecnológica moderna, eficiente e acessível a todos.
          </p>
        </div>
      </div>

      <div class="row g-4">
        <!-- Card 1: Facilitar Denúncias -->
        <div class="col-lg-4 slide-in-left">
          <div class="card card-custom h-100 text-center p-4 hover-lift">
            <div class="card-body">
              <div class="bg-gradient-primary rounded-circle d-inline-flex align-items-center justify-content-center mb-4" style="width: 80px; height: 80px;">
                <i class="fas fa-mobile-alt text-white" style="font-size: 2rem;"></i>
              </div>
              <h4 class="fw-bold mb-3">Facilitar Denúncias</h4>
              <p class="text-muted">
                Simplificar o processo de denúncia de problemas urbanos através de uma 
                interface intuitiva e acessível em qualquer dispositivo.
              </p>
            </div>
          </div>
        </div>

        <!-- Card 2: Agilizar Respostas -->
        <div class="col-lg-4 fade-in" style="animation-delay: 0.2s;">
          <div class="card card-custom h-100 text-center p-4 hover-lift">
            <div class="card-body">
              <div class="bg-gradient-success rounded-circle d-inline-flex align-items-center justify-content-center mb-4" style="width: 80px; height: 80px;">
                <i class="fas fa-clock text-white" style="font-size: 2rem;"></i>
              </div>
              <h4 class="fw-bold mb-3">Agilizar Respostas</h4>
              <p class="text-muted">
                Permitir que a prefeitura receba e processe denúncias de forma mais rápida 
                e organizada, melhorando o tempo de resposta.
              </p>
            </div>
          </div>
        </div>

        <!-- Card 3: Transparência -->
        <div class="col-lg-4 slide-in-right">
          <div class="card card-custom h-100 text-center p-4 hover-lift">
            <div class="card-body">
              <div class="bg-gradient-primary rounded-circle d-inline-flex align-items-center justify-content-center mb-4" style="width: 80px; height: 80px;">
                <i class="fas fa-eye text-white" style="font-size: 2rem;"></i>
              </div>
              <h4 class="fw-bold mb-3">Transparência</h4>
              <p class="text-muted">
                Promover transparência no processo de resolução de problemas urbanos, 
                mantendo o cidadão informado sobre o andamento.
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Seção de impacto -->
      <div class="row mt-5">
        <div class="col-lg-10 mx-auto">
          <div class="card card-custom bg-gradient-primary text-white p-5 hover-lift">
            <div class="row align-items-center">
              <div class="col-lg-8">
                <h3 class="fw-bold mb-3">Impacto Social Positivo</h3>
                <p class="mb-0 opacity-90">
                  Acreditamos que a tecnologia pode ser uma ferramenta poderosa para melhorar 
                  a qualidade de vida nas cidades. Nosso objetivo é criar um ambiente urbano 
                  mais seguro, limpo e organizado para todos os cidadãos.
                </p>
              </div>
              <div class="col-lg-4 text-center">
                <i class="fas fa-heart" style="font-size: 4rem; opacity: 0.8;"></i>
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
  name: 'ObjetivoComponent'
}
</script>

<style scoped>
.fade-in {
  animation: fadeIn 0.8s ease-in;
}

.slide-in-left {
  animation: slideInLeft 0.8s ease-out;
}

.slide-in-right {
  animation: slideInRight 0.8s ease-out;
}

.card {
  border: none;
  transition: all 0.3s ease;
}

.card:hover {
  transform: translateY(-10px);
}

.bg-gradient-primary {
  background: linear-gradient(135deg, var(--primary-blue), var(--accent-blue));
}

.bg-gradient-success {
  background: linear-gradient(135deg, var(--primary-green), var(--accent-green));
}

@media (max-width: 768px) {
  .display-5 {
    font-size: 2rem;
  }
  
  .card {
    margin-bottom: 2rem;
  }
}
</style>

