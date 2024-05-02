<script>
import { ref } from 'vue'

export default {
  setup() {
    const nom = ref('')
    const objet = ref('')
    const message = ref('')
    const nomError = ref('')
    const objetError = ref('')
    const messageError = ref('')

    const validateNom = () => {
      if (!nom.value.trim()) {
        nomError.value = 'Ce champ doit être rempli'
      }
    }

    const validateObjet = () => {
      if (!objet.value.trim()) {
        objetError.value = 'Ce champ doit être rempli'
      }
    }

    const validateMessage = () => {
      if (!message.value.trim()) {
        messageError.value = 'Ce champ doit être rempli'
      }
    }

    const isFormValid = () => {
      return nom.value.trim() && objet.value.trim() && message.value.trim()
    }

    const submitForm = () => {
      if (isFormValid()) {
        window.alert('Merci pour votre message')
        // Utilisation d'une variable d'environnement pour l'adresse du destinataire
        const destinataire = import.meta.env.VITE_EMAIL_ADDRESS
        console.log('Envoyer le message à :', destinataire)
      }
    }

    return {
      nom,
      objet,
      message,
      nomError,
      objetError,
      messageError,
      validateNom,
      validateObjet,
      validateMessage,
      isFormValid,
      submitForm
    }
  }
}
</script>
<template>
  <h1>Contactez moi</h1>
  <form @submit.prevent="submitForm">
    <div>
      <label for="nom">Nom :</label><br />
      <input
        type="text"
        id="nom"
        class="formwidthtxt"
        v-model.trim="nom"
        @focus="nomError = ''"
        @blur="validateNom"
      />
      <span v-if="nomError" style="color: red">{{ nomError }}</span>
    </div>

    <div>
      <label for="objet">Objet :</label><br />
      <input
        type="text"
        id="objet"
        class="formwidthtxt"
        v-model.trim="objet"
        @focus="objetError = ''"
        @blur="validateObjet"
      />
      <span v-if="objetError" style="color: red">{{ objetError }}</span>
    </div>

    <div>
      <label for="message">Message :</label><br />
      <textarea
        id="message"
        class="formwidthmessage"
        v-model.trim="message"
        @focus="messageError = ''"
        @blur="validateMessage"
      ></textarea>
      <span v-if="messageError" style="color: red">{{ messageError }}</span>
    </div>

    <button class="btn" type="submit" v-if="isFormValid">Envoyer</button>
  </form>
</template>
<style scoped>
input[type='text'],
.formwidthtxt {
  width: 50%;
}
.formwidthmessage {
  width: 100%;
}
textarea {
  margin-bottom: 10px;
  width: 100%;
  padding: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}
.btn {
  margin: 5px 350px;
  border-radius: 5px;
  background: linear-gradient(135deg, #427783 0%, #03657e 100%);
  color: whitesmoke;
  width: 25%;
}
</style>
