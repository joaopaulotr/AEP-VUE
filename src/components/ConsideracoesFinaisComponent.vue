<template>
  <section class="section-padding">
    <div class="container">
      <div class="row">
        <div class="col-lg-10 mx-auto">
          <div class="text-center mb-5 fade-in">
            <h2 class="display-5 fw-bold text-primary-custom mb-4">
              Considerações Finais
            </h2>
            <p class="lead">
              Juntos, podemos construir cidades mais inteligentes, eficientes e humanas.
            </p>
          </div>

          <div class="row g-4">
            <!-- Coluna de texto -->
            <div class="col-lg-8 slide-in-left">
              <div class="card card-custom p-4 h-100">
                <h4 class="fw-bold text-success-custom mb-4">
                  O Futuro das Cidades Inteligentes
                </h4>
                <p class="mb-4">
                  A implementação desta plataforma representa um passo importante na direção 
                  de cidades mais inteligentes e conectadas. Através da tecnologia, estamos 
                  criando pontes entre cidadãos e gestores públicos, facilitando a comunicação 
                  e agilizando a resolução de problemas urbanos.
                </p>
                <p class="mb-4">
                  Acreditamos que a participação ativa dos cidadãos é fundamental para o 
                  desenvolvimento urbano sustentável. Nossa plataforma não apenas facilita 
                  essa participação, mas também promove a transparência e a responsabilidade 
                  na gestão pública.
                </p>
                <p class="mb-4">
                  Os resultados esperados vão além da simples resolução de problemas pontuais. 
                  Esperamos contribuir para a criação de uma cultura de colaboração entre 
                  sociedade civil e poder público, onde a tecnologia serve como catalisador 
                  de mudanças positivas.
                </p>
                <div class="d-flex align-items-center">
                  <i class="fas fa-quote-left text-primary-custom me-3" style="font-size: 2rem;"></i>
                  <p class="fst-italic mb-0 text-muted">
                    "A tecnologia é melhor quando aproxima as pessoas." - Matt Mullenweg
                  </p>
                </div>
              </div>
            </div>

            <!-- Coluna de call-to-action -->
            <div class="col-lg-4 slide-in-right">
              <div class="card card-custom bg-gradient-primary text-white p-4 h-100 text-center">
                <div class="card-body d-flex flex-column justify-content-center">
                  <i class="fas fa-rocket mb-4" style="font-size: 4rem; opacity: 0.9;"></i>
                  <h4 class="fw-bold mb-4">Faça Parte da Mudança</h4>
                  <p class="mb-4 opacity-90">
                    Sua participação é essencial para construirmos cidades melhores. 
                    Comece agora mesmo fazendo sua primeira denúncia!
                  </p>
                  <a href="#denuncia" class="btn btn-light btn-lg fw-bold text-primary-custom">
                    <i class="fas fa-plus-circle me-2"></i>
                    Fazer Denúncia
                  </a>
                </div>
              </div>
            </div>
          </div>

          <!-- Seção de agradecimento -->
          <div class="row mt-5">
            <div class="col-12">
              <div class="card card-custom section-bg-light p-5 text-center fade-in" style="animation-delay: 0.3s;">
                <h4 class="fw-bold text-primary-custom mb-4">
                  Agradecimentos
                </h4>
                <p class="lead mb-4">
                  Agradecemos a todos os cidadãos conscientes que acreditam no poder da 
                  tecnologia para transformar nossas cidades. Juntos, estamos construindo 
                  um futuro mais sustentável e organizado.
                </p>
                <div class="row justify-content-center">
                  <div class="col-lg-8">
                    <div class="d-flex justify-content-center align-items-center flex-wrap gap-4">
                      <div class="text-center">
                        <i class="fas fa-heart text-danger mb-2" style="font-size: 2rem;"></i>
                        <p class="small mb-0 fw-semibold">Desenvolvido com amor</p>
                      </div>
                      <div class="text-center">
                        <i class="fas fa-code text-primary-custom mb-2" style="font-size: 2rem;"></i>
                        <p class="small mb-0 fw-semibold">Tecnologia de ponta</p>
                      </div>
                      <div class="text-center">
                        <i class="fas fa-users text-success-custom mb-2" style="font-size: 2rem;"></i>
                        <p class="small mb-0 fw-semibold">Foco no cidadão</p>
                      </div>
                    </div>
                  </div>
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
  name: 'ConsideracoesFinaisComponent'
}
</script>

<style scoped>
.bg-gradient-primary {
  background: linear-gradient(135deg, var(--primary-blue), var(--accent-blue));
}

.card {
  transition: all 0.3s ease;
  border: none;
}

.card:hover {
  transform: translateY(-5px);
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

.btn-light:hover {
  background-color: #ffffff !important;
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
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

