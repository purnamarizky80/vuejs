<template>
  <div>
    <h1>{{ nama }}</h1>
    <input type="text" v-model="nama">
    <br><br>
    Nilai : {{ nilai }}
    <br>    
    <h2>{{ soal1 }}</h2>
    <input type="radio" name="jawaban1" :disabled="checked"> Kusmoro Rusli
    <input type="radio" name="jawaban1" :disabled="checked" @click="benar"> Asep Tapip Yani
    <input type="radio" name="jawaban1" :disabled="checked"> Dadang
    <h2>{{ soal2 }}</h2>
    <input type="radio" name="jawaban2" :disabled="checked2"> Ahmad Heryawan
    <input type="radio" name="jawaban2" :disabled="checked2"> Bejo Sutejo
    <input type="radio" name="jawaban2" :disabled="checked2" @click="benar2"> Ridwan Kamil
    <h2>{{ soal3 }}</h2>
    <input type="radio" name="jawaban3" :disabled="checked3" @click="benar3"> Kusmoro Rusli
    <input type="radio" name="jawaban3" :disabled="checked3" > Herman
    <input type="radio" name="jawaban3" :disabled="checked3"> Encek
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      nama: 'Nama',
      nilai: 0,
      soal1: '1. Siapa Kepala Sekolah SMKN 4 Bandung?',
      soal2: '2. Siapa Gubernur JawaBarat?',
      soal3: '3. Siapa Nama Guru Bahasa Sunda?'
    }
  },
  methods:{
    benar(){
      this.nilai += 1,
      this.checked = true
    },
     benar2(){
      this.nilai += 1,
      this.checked2 = true
    },
     benar3(){
      this.nilai += 1,
      this.checked3 = true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
