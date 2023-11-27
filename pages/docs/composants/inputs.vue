<script setup>
import {
  form,
  inputText,
  inputNombre,
  inputTextWithError,
  textarea,
  inputEmail,
} from "./code/inputs";

definePageMeta({
  layout: "docs",
});

const nom = ref("");
const prenom = ref("");
const description = ref("");
const nombre = ref(0);
const email = ref("");
</script>

<template>
  <Container>
    <TitresH1>Inputs</TitresH1>

    <TextesParagraphe>
      Vous pouvez utilisez les inputs de formulaire dans vos projets.
    </TextesParagraphe>

    <TitresH2>Input de texte</TitresH2>

    <InputsGroup class="max-w-xs">
      <InputsLabel name="nom">Nom</InputsLabel>
      <InputsTexte v-model="nom" name="nom" placeholder="Votre nom" />
    </InputsGroup>

    <div class="mt-1">Valeur du champs: "{{ nom }}"</div>
    <TextesCode :code="inputText" />

    <TitresH2>Input de nombre</TitresH2>

    <InputsGroup class="max-w-xs">
      <InputsLabel name="nombre">Nombre</InputsLabel>
      <InputsNombre
        v-model="nombre"
        name="nombre"
        placeholder="Votre âge"
        :min="0"
        :max="135"
      />
    </InputsGroup>

    <div class="mt-1">Valeur du champs: "{{ nombre }}"</div>
    <TextesCode :code="inputNombre" />

    <TitresH2>Input de Email</TitresH2>

    <InputsGroup class="max-w-xs">
      <InputsLabel name="email">Email</InputsLabel>
      <InputsEmail v-model="email" name="email" placeholder="Votre email" />
    </InputsGroup>

    <div class="mt-1">Valeur du champs: "{{ email }}"</div>
    <TextesCode :code="inputEmail" />

    <TitresH2>Input de texte avec erreur</TitresH2>

    <InputsGroup class="max-w-xs">
      <InputsLabel name="error-nom">Nom*</InputsLabel>
      <InputsTexte v-model="nom" name="error-nom" placeholder="Votre nom" />
      <InputsErreur>Le champs nom est requis</InputsErreur>
    </InputsGroup>

    <TextesCode :code="inputTextWithError" />

    <TitresH2>Textarea</TitresH2>

    <InputsGroup class="max-w-xs">
      <InputsLabel name="description">Description</InputsLabel>
      <InputsTextarea
        v-model="description"
        name="description"
        placeholder="Votre texte ..."
        rows="10"
      />
    </InputsGroup>
    <div class="mt-1">Valeur du champs: "{{ description }}"</div>

    <TextesCode :code="textarea" />

    <TitresH2>Form</TitresH2>

    <InputsForm>
      <InputsGroup class="max-w-xs">
        <InputsLabel name="form-nom">Nom</InputsLabel>
        <InputsTexte v-model="nom" name="form-nom" placeholder="Votre nom" />
      </InputsGroup>

      <InputsGroup class="max-w-xs">
        <InputsLabel name="form-prenom">Prénom</InputsLabel>
        <InputsTexte
          v-model="prenom"
          name="form-prenom"
          placeholder="Votre prénom"
        />
      </InputsGroup>

      <InputsGroup class="max-w-xs">
        <InputsLabel name="form-description">Description</InputsLabel>
        <InputsTextarea
          v-model="description"
          name="form-description"
          placeholder="Votre texte ..."
          rows="10"
        />
      </InputsGroup>
    </InputsForm>

    <TextesCode :code="form" />
  </Container>
</template>
