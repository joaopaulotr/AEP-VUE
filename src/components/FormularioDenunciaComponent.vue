<template>
  <section id="denuncia" class="section-padding section-bg-light">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 mx-auto text-center mb-5 fade-in">
          <h2 class="display-5 fw-bold text-primary-custom mb-4">
            Fazer Denúncia
          </h2>
          <p class="lead">
            Relate um problema urbano em sua região. Sua denúncia é importante 
            para melhorar a qualidade de vida na cidade.
          </p>
        </div>
      </div>

      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="card card-custom p-4 p-md-5">
            <!-- Alerta de sucesso -->
            <div v-if="showSuccessAlert" class="alert alert-success alert-dismissible fade show" role="alert">
              <i class="fas fa-check-circle me-2"></i>
              <strong>Denúncia enviada com sucesso!</strong> 
              Você receberá um e-mail de confirmação em breve.
              <button type="button" class="btn-close" @click="showSuccessAlert = false"></button>
            </div>

            <!-- Alerta de erro -->
            <div v-if="showErrorAlert" class="alert alert-danger alert-dismissible fade show" role="alert">
              <i class="fas fa-exclamation-triangle me-2"></i>
              <strong>Erro ao enviar denúncia!</strong> 
              {{ errorMessage }}
              <button type="button" class="btn-close" @click="showErrorAlert = false"></button>
            </div>

            <form @submit.prevent="submitForm" novalidate>
              <div class="row g-4">
                <!-- Nome Completo -->
                <div class="col-md-6">
                  <label for="nomeCompleto" class="form-label fw-semibold">
                    <i class="fas fa-user me-2 text-primary-custom"></i>
                    Nome Completo *
                  </label>
                  <input 
                    type="text" 
                    class="form-control form-control-custom"
                    :class="{ 'is-invalid': errors.nomeCompleto }"
                    id="nomeCompleto"
                    v-model="form.nomeCompleto"
                    placeholder="Digite seu nome completo"
                    @blur="validateField('nomeCompleto')"
                  >
                  <div v-if="errors.nomeCompleto" class="invalid-feedback">
                    {{ errors.nomeCompleto }}
                  </div>
                </div>

                <!-- E-mail -->
                <div class="col-md-6">
                  <label for="email" class="form-label fw-semibold">
                    <i class="fas fa-envelope me-2 text-primary-custom"></i>
                    E-mail *
                  </label>
                  <input 
                    type="email" 
                    class="form-control form-control-custom"
                    :class="{ 'is-invalid': errors.email }"
                    id="email"
                    v-model="form.email"
                    placeholder="seu@email.com"
                    @blur="validateField('email')"
                  >
                  <div v-if="errors.email" class="invalid-feedback">
                    {{ errors.email }}
                  </div>
                </div>

                <!-- Tipo de Ocorrência -->
                <div class="col-md-6">
                  <label for="tipoOcorrencia" class="form-label fw-semibold">
                    <i class="fas fa-list me-2 text-primary-custom"></i>
                    Tipo de Ocorrência *
                  </label>
                  <select 
                    class="form-select form-control-custom"
                    :class="{ 'is-invalid': errors.tipoOcorrencia }"
                    id="tipoOcorrencia"
                    v-model="form.tipoOcorrencia"
                    @change="validateField('tipoOcorrencia')"
                  >
                    <option value="">Selecione o tipo de problema</option>
                    <option value="buraco-rua">Buraco na rua</option>
                    <option value="lixo-acumulado">Lixo acumulado</option>
                    <option value="poste-sem-luz">Poste sem iluminação</option>
                    <option value="arvore-caida">Árvore caída</option>
                    <option value="calcada-danificada">Calçada danificada</option>
                    <option value="semaforo-defeito">Semáforo com defeito</option>
                    <option value="vazamento-agua">Vazamento de água</option>
                    <option value="esgoto-entupido">Esgoto entupido</option>
                    <option value="pichacao">Pichação/Vandalismo</option>
                    <option value="outros">Outros</option>
                  </select>
                  <div v-if="errors.tipoOcorrencia" class="invalid-feedback">
                    {{ errors.tipoOcorrencia }}
                  </div>
                </div>

                <!-- Localização -->
                <div class="col-md-6">
                  <label for="localizacao" class="form-label fw-semibold">
                    <i class="fas fa-map-marker-alt me-2 text-primary-custom"></i>
                    Localização *
                  </label>
                  <div class="input-group">
                    <input 
                      type="text" 
                      class="form-control form-control-custom"
                      :class="{ 'is-invalid': errors.localizacao }"
                      id="localizacao"
                      v-model="form.localizacao"
                      placeholder="Endereço ou ponto de referência"
                      @blur="validateField('localizacao')"
                    >
                    <button 
                      class="btn btn-outline-primary" 
                      type="button"
                      @click="getCurrentLocation"
                      :disabled="gettingLocation"
                    >
                      <i class="fas fa-crosshairs" :class="{ 'fa-spin': gettingLocation }"></i>
                    </button>
                  </div>
                  <div v-if="errors.localizacao" class="invalid-feedback">
                    {{ errors.localizacao }}
                  </div>
                  <small class="form-text text-muted">
                    Clique no ícone para usar sua localização atual
                  </small>
                </div>

                <!-- Descrição -->
                <div class="col-12">
                  <label for="descricao" class="form-label fw-semibold">
                    <i class="fas fa-comment-alt me-2 text-primary-custom"></i>
                    Descrição do Problema *
                  </label>
                  <textarea 
                    class="form-control form-control-custom"
                    :class="{ 'is-invalid': errors.descricao }"
                    id="descricao"
                    rows="4"
                    v-model="form.descricao"
                    placeholder="Descreva detalhadamente o problema encontrado..."
                    @blur="validateField('descricao')"
                  ></textarea>
                  <div v-if="errors.descricao" class="invalid-feedback">
                    {{ errors.descricao }}
                  </div>
                  <small class="form-text text-muted">
                    Mínimo de 20 caracteres. Seja específico para facilitar a resolução.
                  </small>
                </div>

                <!-- Upload de Imagem -->
                <div class="col-12">
                  <label for="imagem" class="form-label fw-semibold">
                    <i class="fas fa-camera me-2 text-primary-custom"></i>
                    Foto do Problema
                  </label>
                  <div class="upload-area" 
                       :class="{ 'dragover': isDragOver, 'has-file': form.imagem }"
                       @dragover.prevent="isDragOver = true"
                       @dragleave.prevent="isDragOver = false"
                       @drop.prevent="handleFileDrop">
                    <input 
                      type="file" 
                      class="form-control d-none"
                      id="imagem"
                      ref="fileInput"
                      accept="image/*"
                      @change="handleFileSelect"
                    >
                    
                    <div v-if="!form.imagem" class="upload-content text-center p-4">
                      <i class="fas fa-cloud-upload-alt mb-3" style="font-size: 3rem; color: var(--primary-blue);"></i>
                      <p class="mb-2 fw-semibold">Arraste uma imagem aqui ou clique para selecionar</p>
                      <p class="text-muted small mb-3">Formatos aceitos: JPG, PNG, GIF (máx. 5MB)</p>
                      <button type="button" class="btn btn-outline-primary" @click="$refs.fileInput.click()">
                        <i class="fas fa-plus me-2"></i>Selecionar Arquivo
                      </button>
                    </div>

                    <div v-else class="upload-preview text-center p-4">
                      <img :src="imagePreview" alt="Preview" class="img-thumbnail mb-3" style="max-height: 200px;">
                      <p class="mb-2 fw-semibold">{{ form.imagem.name }}</p>
                      <p class="text-muted small mb-3">{{ formatFileSize(form.imagem.size) }}</p>
                      <button type="button" class="btn btn-outline-danger" @click="removeFile">
                        <i class="fas fa-trash me-2"></i>Remover
                      </button>
                    </div>
                  </div>
                </div>

                <!-- Botões -->
                <div class="col-12">
                  <div class="d-flex justify-content-between align-items-center">
                    <small class="text-muted">
                      <i class="fas fa-info-circle me-1"></i>
                      Campos marcados com * são obrigatórios
                    </small>
                    <div class="d-flex gap-3">
                      <button type="button" class="btn btn-outline-secondary" @click="resetForm">
                        <i class="fas fa-undo me-2"></i>Limpar
                      </button>
                      <button type="submit" class="btn btn-success-custom btn-lg" :disabled="isSubmitting">
                        <span v-if="isSubmitting">
                          <i class="fas fa-spinner fa-spin me-2"></i>Enviando...
                        </span>
                        <span v-else>
                          <i class="fas fa-paper-plane me-2"></i>Enviar Denúncia
                        </span>
                      </button>
                    </div>
                  </div>
                </div>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FormularioDenunciaComponent',
  data() {
    return {
      form: {
        nomeCompleto: '',
        email: '',
        tipoOcorrencia: '',
        localizacao: '',
        descricao: '',
        imagem: null
      },
      errors: {},
      showSuccessAlert: false,
      showErrorAlert: false,
      errorMessage: '',
      isSubmitting: false,
      isDragOver: false,
      gettingLocation: false,
      imagePreview: null
    }
  },
  methods: {
    validateField(fieldName) {
      this.errors = { ...this.errors };
      delete this.errors[fieldName];

      switch (fieldName) {
        case 'nomeCompleto':
          if (!this.form.nomeCompleto.trim()) {
            this.errors.nomeCompleto = 'Nome completo é obrigatório';
          } else if (this.form.nomeCompleto.trim().length < 3) {
            this.errors.nomeCompleto = 'Nome deve ter pelo menos 3 caracteres';
          }
          break;

        case 'email':
          const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
          if (!this.form.email.trim()) {
            this.errors.email = 'E-mail é obrigatório';
          } else if (!emailRegex.test(this.form.email)) {
            this.errors.email = 'E-mail inválido';
          }
          break;

        case 'tipoOcorrencia':
          if (!this.form.tipoOcorrencia) {
            this.errors.tipoOcorrencia = 'Selecione o tipo de ocorrência';
          }
          break;

        case 'localizacao':
          if (!this.form.localizacao.trim()) {
            this.errors.localizacao = 'Localização é obrigatória';
          } else if (this.form.localizacao.trim().length < 5) {
            this.errors.localizacao = 'Localização deve ser mais específica';
          }
          break;

        case 'descricao':
          if (!this.form.descricao.trim()) {
            this.errors.descricao = 'Descrição é obrigatória';
          } else if (this.form.descricao.trim().length < 20) {
            this.errors.descricao = 'Descrição deve ter pelo menos 20 caracteres';
          }
          break;
      }
    },

    validateForm() {
      this.validateField('nomeCompleto');
      this.validateField('email');
      this.validateField('tipoOcorrencia');
      this.validateField('localizacao');
      this.validateField('descricao');

      return Object.keys(this.errors).length === 0;
    },

    async submitForm() {
      if (!this.validateForm()) {
        this.showErrorAlert = true;
        this.errorMessage = 'Por favor, corrija os erros no formulário.';
        return;
      }

      this.isSubmitting = true;
      this.showErrorAlert = false;

      try {
        // Configuração do EmailJS (substitua pelos seus IDs)
        const emailjs = await import('@emailjs/browser');
        
        // Dados para o template de e-mail
        const templateParams = {
          from_name: this.form.nomeCompleto,
          from_email: this.form.email,
          tipo_ocorrencia: this.form.tipoOcorrencia,
          localizacao: this.form.localizacao,
          descricao: this.form.descricao,
          to_email: this.form.email, // E-mail de confirmação para o usuário
          reply_to: this.form.email
        };

        // Enviar e-mail de confirmação para o usuário
        // NOTA: Para usar em produção, você precisa configurar sua conta EmailJS
        // e substituir os IDs abaixo pelos seus próprios IDs
        /*
        await emailjs.send(
          'YOUR_SERVICE_ID',    // Substitua pelo seu Service ID
          'YOUR_TEMPLATE_ID',   // Substitua pelo seu Template ID
          templateParams,
          'YOUR_PUBLIC_KEY'     // Substitua pela sua Public Key
        );
        */

        // Simulação de envio bem-sucedido
        await new Promise(resolve => setTimeout(resolve, 2000));
        
        console.log('Dados da denúncia:', {
          ...this.form,
          timestamp: new Date().toISOString()
        });
        
        this.showSuccessAlert = true;
        this.resetForm();
        
        // Scroll para o topo do formulário
        document.getElementById('denuncia').scrollIntoView({ 
          behavior: 'smooth', 
          block: 'start' 
        });
        
      } catch (error) {
        console.error('Erro ao enviar denúncia:', error);
        this.showErrorAlert = true;
        this.errorMessage = 'Erro ao enviar denúncia. Tente novamente em alguns minutos.';
      } finally {
        this.isSubmitting = false;
      }
    },

    resetForm() {
      this.form = {
        nomeCompleto: '',
        email: '',
        tipoOcorrencia: '',
        localizacao: '',
        descricao: '',
        imagem: null
      };
      this.errors = {};
      this.imagePreview = null;
      this.showSuccessAlert = false;
      this.showErrorAlert = false;
    },

    handleFileSelect(event) {
      const file = event.target.files[0];
      this.processFile(file);
    },

    handleFileDrop(event) {
      this.isDragOver = false;
      const file = event.dataTransfer.files[0];
      this.processFile(file);
    },

    processFile(file) {
      if (!file) return;

      // Validar tipo de arquivo
      if (!file.type.startsWith('image/')) {
        alert('Por favor, selecione apenas arquivos de imagem.');
        return;
      }

      // Validar tamanho (5MB)
      if (file.size > 5 * 1024 * 1024) {
        alert('O arquivo deve ter no máximo 5MB.');
        return;
      }

      this.form.imagem = file;
      
      // Criar preview
      const reader = new FileReader();
      reader.onload = (e) => {
        this.imagePreview = e.target.result;
      };
      reader.readAsDataURL(file);
    },

    removeFile() {
      this.form.imagem = null;
      this.imagePreview = null;
      this.$refs.fileInput.value = '';
    },

    formatFileSize(bytes) {
      if (bytes === 0) return '0 Bytes';
      const k = 1024;
      const sizes = ['Bytes', 'KB', 'MB'];
      const i = Math.floor(Math.log(bytes) / Math.log(k));
      return parseFloat((bytes / Math.pow(k, i)).toFixed(2)) + ' ' + sizes[i];
    },

    async getCurrentLocation() {
      if (!navigator.geolocation) {
        alert('Geolocalização não é suportada pelo seu navegador.');
        return;
      }

      this.gettingLocation = true;

      navigator.geolocation.getCurrentPosition(
        async (position) => {
          try {
            // Aqui você pode usar uma API de geocoding reverso
            // Por simplicidade, vamos usar coordenadas
            const lat = position.coords.latitude.toFixed(6);
            const lng = position.coords.longitude.toFixed(6);
            this.form.localizacao = `Lat: ${lat}, Lng: ${lng}`;
          } catch (error) {
            console.error('Erro ao obter endereço:', error);
            alert('Erro ao obter localização. Digite manualmente.');
          } finally {
            this.gettingLocation = false;
          }
        },
        (error) => {
          console.error('Erro de geolocalização:', error);
          alert('Erro ao acessar localização. Verifique as permissões.');
          this.gettingLocation = false;
        }
      );
    }
  }
}
</script>

<style scoped>
.upload-area {
  border: 2px dashed #dee2e6;
  border-radius: 8px;
  transition: all 0.3s ease;
  cursor: pointer;
}

.upload-area:hover,
.upload-area.dragover {
  border-color: var(--primary-blue);
  background-color: rgba(37, 99, 235, 0.05);
}

.upload-area.has-file {
  border-color: var(--primary-green);
  background-color: rgba(22, 163, 74, 0.05);
}

.upload-content,
.upload-preview {
  transition: all 0.3s ease;
}

.form-control-custom {
  border: 2px solid #e5e7eb;
  border-radius: 8px;
  padding: 12px 16px;
  transition: all 0.3s ease;
}

.form-control-custom:focus {
  border-color: var(--primary-blue);
  box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
}

.btn-success-custom {
  background: linear-gradient(135deg, var(--primary-green), var(--accent-green));
  border: none;
  border-radius: 8px;
  padding: 12px 24px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.btn-success-custom:hover:not(:disabled) {
  background: linear-gradient(135deg, var(--accent-green), var(--primary-green));
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(22, 163, 74, 0.3);
}

.btn-success-custom:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

.card {
  border: none;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.alert {
  border-radius: 8px;
  border: none;
}

@media (max-width: 768px) {
  .d-flex.justify-content-between {
    flex-direction: column;
    gap: 1rem;
  }
  
  .d-flex.gap-3 {
    justify-content: center;
  }
}
</style>

