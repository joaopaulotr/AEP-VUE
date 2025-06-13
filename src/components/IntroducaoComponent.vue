<template>
  <section id="inicio" class="section-padding">
    <div class="container">
      <div class="row align-items-center">
        <!-- Coluna do texto -->
        <div class="col-lg-6 fade-in">
          <h1 class="display-4 fw-bold text-primary-custom mb-4">
            Transformando Cidades com Tecnologia
          </h1>
          <p class="lead mb-4">
            Vivemos em um mundo onde os problemas urbanos afetam diariamente a qualidade de vida dos cidadãos. 
            Buracos nas ruas, lixo acumulado, postes sem iluminação, árvores caídas e muitos outros problemas 
            precisam de uma solução rápida e eficiente.
          </p>
          <p class="mb-4">
            Nossa plataforma surge como uma ponte entre você, cidadão consciente, e a prefeitura da sua cidade. 
            Através da tecnologia, facilitamos o processo de denúncia e acompanhamento de problemas urbanos, 
            promovendo uma cidade mais organizada e segura para todos.
          </p>
          <div class="d-flex flex-wrap gap-3">
            <a href="#denuncia" class="btn btn-primary-custom btn-lg">
              <i class="fas fa-plus-circle me-2"></i>
              Fazer Denúncia
            </a>
            <a href="#objetivo" class="btn btn-outline-primary btn-lg">
              <i class="fas fa-info-circle me-2"></i>
              Saiba Mais
            </a>
          </div>
        </div>

        <!-- Coluna da imagem/ícones -->
        <div class="col-lg-6 mt-5 mt-lg-0 slide-in-right">
          <div class="row g-4">
            <div class="col-6">
              <div class="card card-custom text-center p-4 hover-lift">
                <i class="fas fa-road icon-large text-danger"></i>
                <h5 class="fw-bold">Buracos nas Ruas</h5>
                <p class="text-muted mb-0">Problemas de pavimentação</p>
              </div>
            </div>
            <div class="col-6">
              <div class="card card-custom text-center p-4 hover-lift">
                <i class="fas fa-trash icon-large text-warning"></i>
                <h5 class="fw-bold">Lixo Acumulado</h5>
                <p class="text-muted mb-0">Coleta inadequada</p>
              </div>
            </div>
            <div class="col-6">
              <div class="card card-custom text-center p-4 hover-lift">
                <i class="fas fa-lightbulb icon-large text-dark"></i>
                <h5 class="fw-bold">Iluminação</h5>
                <p class="text-muted mb-0">Postes sem luz</p>
              </div>
            </div>
            <div class="col-6">
              <div class="card card-custom text-center p-4 hover-lift">
                <i class="fas fa-tree icon-large text-success"></i>
                <h5 class="fw-bold">Árvores Caídas</h5>
                <p class="text-muted mb-0">Riscos à segurança</p>
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
  name: 'IntroducaoComponent'
}
</script>

<style scoped>
.card {
  transition: all 0.3s ease;
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
}

.icon-large {
  font-size: 3rem;
  margin-bottom: 1rem;
}

@media (max-width: 768px) {
  .display-4 {
    font-size: 2.5rem;
  }
  
  .icon-large {
    font-size: 2rem;
  }
  
  .card {
    padding: 1.5rem !important;
  }
}
</style>

