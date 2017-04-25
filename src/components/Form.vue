<template>
  <div class="">
    {{ formFields }}
    <div class="columns is-multiline">
      <div class="column is-4">
        <div class="field">
          <label class="label">Nome *</label>
          <p class="control">
            <input :class="{ 'input': true, 'is-danger': true }" type="text" placeholder="Informe seu nome completo" v-model="formFields.name">
          </p>
          <p class="help is-danger">Informe corretamente seu nome.</p>
        </div>
      </div>
      <div class="column is-3">
        <div class="field">
          <label class="label">E-mail *</label>
          <p class="control">
            <input :class="{ 'input': true, 'is-danger': true }" type="email" placeholder="Informe seu e-mail" v-model="formFields.email">
          </p>
          <p class="help is-danger">Informe corretamente seu e-mail.</p>
        </div>
      </div>
      <div class="column is-3">
        <div class="field">
          <label class="label">Telefone *</label>
          <p class="control">
            <input :class="{ 'input': true, 'is-danger': true }" type="text" placeholder="(11) 99876-5432" v-model="formFields.phone">
          </p>
          <p class="help is-danger">Informe um telefone de contato.</p>
        </div>
      </div>
      <div class="column">
        <div class="field">
          <label class="label">Orçamento?</label>
          <p class="control">
            <switches v-model="formFields.quote"
                      :selected="formFields.quote"
                      text-enabled="Sim"
                      text-disabled="Não"
                      :type-bold="true"
                      color="green"
                      theme="bulma"></switches>
          </p>
        </div>
      </div>
      <div class="column is-4">
        <div class="columns is-multiline">
          <div class="column is-10">
            <div class="field">
              <label class="label">Como soube da JMOB? *</label>
              <p class="control">
                <span class="select">
                  <select v-model="formFields.hearAboutUs" @change="setHearAboutUsDetails()">
                    <option value="">Selecione uma opção</option>
                    <option :value="option" v-for="option in selectOptions">{{ option }}</option>
                  </select>
                </span>
              </p>
              <p class="help is-danger">Selecione uma das opções.</p>
            </div>
          </div>
          <div class="column" v-show="formFields.hearAboutUs === 'Indicação' || formFields.hearAboutUs === 'Outro'">
            <div class="field">
              <label class="label">{{ hearAboutUs.label }}</label>
              <p class="control">
                <input :class="{ 'input': true, 'is-danger': true }" type="text" :placeholder="hearAboutUs.placeholder" v-model="formFields.hearAboutUsDetail">
              </p>
              <p class="help is-danger">{{ hearAboutUs.error }}</p>
            </div>
          </div>
        </div>
      </div>
      <div class="column is-6">
        <div class="field">
          <label class="label">Comentários</label>
          <p class="control">
            <textarea :class="{ 'textarea': true, 'is-danger': true }" type="text" placeholder="Informe seu nome completo" v-model="formFields.description"></textarea>
          </p>
        </div>
      </div>
    </div>
    <div class="columns is=multiline">
      <div class="column">
        <button class="button is-primary">Enviar mensagem</button>
      </div>
    </div>
  </div>
</template>

<script>
import Switches from 'vue-switches'
export default {
  data () {
    return {
      formFields: {
        name: '',
        email: '',
        phone: '',
        quote: false,
        description: '',
        hearAboutUs: '',
        hearAboutUsDetail: ''
      },
      hearAboutUs: {
        label: '',
        placeholder: '',
        error: ''
      },
      selectOptions: [
        'Google',
        'Facebook',
        'Instagram',
        'Anúncio na TV',
        'Anúncio na rádio',
        'Indicação',
        'Outro'
      ]
    }
  },
  methods: {
    setHearAboutUsDetails () {
      this.hearAboutUs.label = 'Indicação *'
      this.hearAboutUs.placeholder = 'Informe a pessoa da indicação'
      this.hearAboutUs.error = 'Campo requerido.'
      if (this.formFields.hearAboutUs === 'Outro') {
        this.hearAboutUs.label = 'Por favor, detalhe *'
        this.hearAboutUs.placeholder = 'Detalhe como soube'
        this.hearAboutUs.error = 'Por favor, informe como chegou até nós.'
      }
    }
  },
  components: {
    Switches
  }
}
</script>

<style lang="css">
</style>
