<template>
    <div>
      <h2>Formulir</h2>
      <form @submit.prevent="submitForm">
        <label for="">Nama :</label>
        <input class= "{'is-invalid':isInvalidName}" text nama="name" v-model="siswa.nama">
        <div v-if = "isInvalidNama" class="error-message"></div>
        <br>
        <label for="">Kelas:</label>
        <input class = "{'is-invalid': isInvalidKelas}"  type="text" name="kelas" v-model="siswa.kelas">
        <div v-if="isInvalidKelas" class="error-massage"></div>
        <br>
        <label for="">Alamat:</label>
        <input class = "{'is-invalid': isInvalidAlamat}"  type="text" name="alamat" v-model="siswa.alamat">
        <div v-if="isInvalidAlamat" class="error-massage"></div>
        <br>
        <label for="">Nilai Matematika:</label>
        <input class = "{'is-invalid': isInvalidNilaimatematika}"  type="text" name="nilaimatematika" v-model="siswa.nilaimatematika">
        <div v-if="isInvalidNilaimatematika" class="error-massage"></div>
        <br>
        <label for="">Nilai Bahasa indonesia:</label>
        <input class = "{'is-invalid': isInvalidNilaibahasaindonesia}"  type="text" name="nilaibahasaindonesia" v-model="siswa.nilaibahasaindonesia">
        <div v-if="isInvalidNilaibahasaindonesia" class="error-massage"></div>
        <br>
        <label for="">Nilai ipa:</label>
        <input class = "{'is-invalid': isInvalidNilaiipa}"  type="text" name="nilaiipa" v-model="siswa.nilaiipa">
        <div v-if=" isInvalidNilaiipa" class="error-massage"></div>
        <br>

        <button type="submit">Simpan</button>
      </form>
      <div v-if="showResult">
        nama : {{ nama }} <br>
        kelas : {{ kelas }} <br>
        alamt : {{ alamat }} <br>
        Nilai Matematika: {{ nilaimatematika }} <br>
        Nilai Bahasa indonesia: {{ nilaibahasaindonesia }} <br>
        Nilai ipa: {{ nilaiipa }} <br>
        total : {{ total }} <br>
        keterangan : {{ keterangan }} <br>
      </div>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    data() {
      return {
        siswa: {
          nama: '',
          kelas: '',
          alamat: '',
          nilaimatematika: '',
          nilaibahasaindonesia: '',
          nilaiipa: '',
        },
        showResult: ref(false),
        nama: ref(''),
        kelas: ref(''),
        alamat: ref(''),
        nilaimatematika: ref(''),
        nilaibahasaindonesia: ref(''),
        nilaiipa: ref(''),
        total: 0,
        keterangan: ref(''),
      };
    },
    computed: {
        isInvalidName(){
            return this.siswa.nama.length <= 1;
        },
        isInvalidKelas(){
            return this.siswa.kelas.length <= 1;
        },
        isInvalidAlamat(){
            return this.siswa.alamat.length <= 1;
        },
        isInvalidNilaimatematika(){
            return this.siswa.nilaimatematika.length <= 1; 
        },
        isInvalidNilaibahasaindonesia(){
            return this.siswa.nilaibahasaindonesia.length <= 1;
        },
        isInvalidNilaiipa(){
            return this.siswa.nilaiipa.length <= 1;
        }

    },
    methods: {
      submitForm() {
        this.nama = this.siswa.nama;
        this.kelas = this.siswa.kelas;
        this.alamat = this.siswa.alamat;
        this.nilaimatematika = this.siswa.nilaimatematika;
        this.nilaibahasaindonesia = this.siswa.nilaibahasaindonesia;
        this.nilaiipa = this.siswa.nilaiipa
        this.total = parseInt(this.nilaimatematika) + parseInt(this.nilaibahasaindonesia) + parseInt(this.nilaiipa)
        if (this.total > 240 ){
            this.keterangan = "Lulus"
        } else {
            this.keterangan = "Tidak lulus"
        }
        this.showResult = true;
      }
    },
  };
  </script>
  
  <style>
  h2 {
    color: black;
  }
  .error-message {
    color: black;
    margin-top: 5px;
  }
  .is-invalid {
    border-color: blueviolet;
  }
  </style>