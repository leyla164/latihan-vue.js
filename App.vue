<template>
    <div>
      <h2>Formulir</h2>
      <form @submit.prevent="submitForm">
        <label for="">Nama:</label>
        <input class= "{'is-invalid':isInvalidName}"
        text name="nama" v-model="kontak.nama">
        <div v-if = "isInvalidName" class="error-message"> 
            Nama harus di isi!     
        </div>
        <br>
        <label for="">Email:</label>
        <input class = "{'is-invalid': isInvalidEmail}"
        type="email" name="email" v-model="kontak.email">
        <div v-if="isInvalidEmail" class="error-massage">
            Email harus di isi!
        </div>
        <br>
        <button type="submit">Simpan</button>
      </form>
      <div v-if="showResult">
        nama : {{ name }} <br>
        email : {{ email }}
      </div>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    data() {
      return {
        kontak: {
          nama: '',
          email: '',
        },
        showResult: ref(false),
        name: ref(''),
        email: ref(''),
      };
    },
    computed: {
        isInvalidName(){
            return this.kontak.nama.length <= 1;
        },
        isInvalidEmail(){
            return this.kontak.email.length <= 0;
        }
    },
    methods: {
      submitForm() {
        this.name = this.kontak.nama;
        this.email = this.kontak.email;
        this.showResult = true;
        this.isInvalidEmail = false;
        this.isInvalidName = false;
      },
    },
  };
  </script>
  
  <style>
  h2 {
    color: black;
  }
  .error-message {
    color: blueviolet;
    margin-top: 5px;
  }
  .is-invalid {
    border-color: blueviolet;
  }
  </style>