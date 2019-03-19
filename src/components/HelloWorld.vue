<template>
  <div class="hello">
  <center>
  <div v-if="show">
  <table><center><h1>Quiz</h1></center><hr><br>
    <div class="soal1" v-for="soal in soal1" v-bind:key="soal.soal1">
      <tr>
           <td><b>{{ soal.no }}.</b> {{ soal.soal }}</td> 
      </tr>
      <tr>
        <div class="Divide">
            <td>
              <input type="radio" name="soal1" value="a" v-model="picked1">{{soal.jaw_a}}
              <input type="radio" name="soal1" value="b" v-model="picked1">{{soal.jaw_b}}
              <input type="radio" name="soal1" value="c" v-model="picked1">{{soal.jaw_c}}
              <input type="radio" name="soal1" value="d" v-model="picked1">{{soal.jaw_d}}
              <input type="radio" name="soal1" value="e" v-model="picked1">{{soal.jaw_e}}
            </td>
        </div>
      </tr><br><hr>
    </div>
    <br>
    <div class="soal2" v-for="soal in soal2" v-bind:key="soal.soal2">
      <tr>
           <td><b>{{ soal.no }}.</b> {{ soal.soal }}</td>
      </tr>
      <tr>
        <div class="Divide">
            <td>
              <input type="radio" name="soal2" value="a" v-model="picked2">{{soal.jaw_a}}
              <input type="radio" name="soal2" value="b" v-model="picked2">{{soal.jaw_b}}
              <input type="radio" name="soal2" value="c" v-model="picked2">{{soal.jaw_c}}
              <input type="radio" name="soal2" value="d" v-model="picked2">{{soal.jaw_d}}
              <input type="radio" name="soal2" value="e" v-model="picked2">{{soal.jaw_e}}
            </td>
        </div>
      </tr><br><hr><br>
    </div>
    <div class="soal3" v-for="soal in soal3" v-bind:key="soal.soal3">
      <tr>
           <td><b>{{ soal.no }}.</b> {{ soal.soal }}</td>
      </tr>
      <tr>
        <div class="Divide">
            <td>
              <input type="radio" name="soal3" value="a" v-model="picked3">{{soal.jaw_a}}
              <input type="radio" name="soal3" value="b" v-model="picked3">{{soal.jaw_b}}
              <input type="radio" name="soal3" value="c" v-model="picked3">{{soal.jaw_c}}
              <input type="radio" name="soal3" value="d" v-model="picked3">{{soal.jaw_d}}
              <input type="radio" name="soal3" value="e" v-model="picked3">{{soal.jaw_e}}
            </td>
        </div>
      </tr><br><hr><br>
    </div>
     <div class="soal4" v-for="soal in soal4" v-bind:key="soal.soal4">
      <tr>
           <td><b>{{ soal.no }}.</b> {{ soal.soal }}</td>
      </tr>
      <tr>
        <div class="Divide">
            <td>
              <input type="radio" name="soal4" value="a" v-model="picked4">{{soal.jaw_a}}
              <input type="radio" name="soal4" value="b" v-model="picked4">{{soal.jaw_b}}
              <input type="radio" name="soal4" value="c" v-model="picked4">{{soal.jaw_c}}
              <input type="radio" name="soal4" value="d" v-model="picked4">{{soal.jaw_d}}
              <input type="radio" name="soal4" value="e" v-model="picked4">{{soal.jaw_e}}
            </td>
        </div>
      </tr><br><hr><br>
    </div>
    <div class="soal5" v-for="soal in soal5" v-bind:key="soal.soal5">
      <tr>
           <td><b>{{ soal.no }}.</b> {{ soal.soal }}</td>
      </tr>
      <tr>
        <div class="Divide">
            <td>
              <input type="radio" name="soal5" value="a" v-model="picked5">{{soal.jaw_a}}
              <input type="radio" name="soal5" value="b" v-model="picked5">{{soal.jaw_b}}
              <input type="radio" name="soal5" value="c" v-model="picked5">{{soal.jaw_c}}
              <input type="radio" name="soal5" value="d" v-model="picked5">{{soal.jaw_d}}
              <input type="radio" name="soal5" value="e" v-model="picked5">{{soal.jaw_e}}
            </td>
        </div>
      </tr><br><hr>
    </div>
    </table>
    </div>
    <div v-else>
      <h1>Hasil Akhir</h1>
      <h1>Nilai: {{ nilai() }}</h1>
      <h2>Jawaban benar : {{jumlah_benar() }}</h2>
      <h2>Jawaban salah : {{jumlah_salah() }}</h2>
    </div>
    <button v-if="btnShow" type="button" v-on:click="hideTitle">Submit</button>
    </center>
  </div>
</template>

<script>
export default {
  name: 'Agung Rizki',
  data () {
    return {
      msg: 'Quiz',
      show:true,
      btnShow:true,
      picked1:'',picked2:'',picked3:'',picked4:'',picked5:'',
      soal1:[
      {
        no:'1',
        soal:"Izin yang diperlukan wirausahawan untuk menjalankan usaha perdagangan serta terdata usaha perdagangannya di pemerintah, adalah izin",
        jaw_a:"A. NRB",
        jaw_b:"B. AMDAL",
        jaw_c:"C. SITU",
        jaw_d:"D. NRP",
        jaw_e:"E. SIUP"
      }
      ],
      soal2:[
      {
        no:'2',
        soal:"Pada sikap lilin, posisi tangan berada pada",
        jaw_a:"A. Kedua Paha",
        jaw_b:"B. Kedua Pinggang",
        jaw_c:"C. Atas Kepala",
        jaw_d:"D. Samping Telinga",
        jaw_e:"E. Di Kedua Kaki"
      }
    ],
      soal3:[
      {
        no:'3',
        soal:"Salah satu unsur seni rupa paling menonjol yang terdapat dalam lukisan ekspresionisme karya affandi adalah",
        jaw_a:"A. Titik",
        jaw_b:"B. Garis",
        jaw_c:"C. Warna",
        jaw_d:"D. Tekstur",
        jaw_e:"E. Gelap Terang"
      }
    ],
      soal4:[
      {
        no:'4',
        soal:"Ibu Kota Indonesia berada di provinsi ",
        jaw_a:"A. JawaBarat",
        jaw_b:"B. Banten",
        jaw_c:"C. Jaya Pura",
        jaw_d:"D. Jakarta",
        jaw_e:"E. Riau"
      }
    ],
      soal5:[
      {
        no:'5',
        soal:"Taman Hutan Raya Ir Djuanda terletak di",
        jaw_a:"A. Bandung",
        jaw_b:"B. Jakarta",
        jaw_c:"C. Palu",
        jaw_d:"D. Malang",
        jaw_e:"E. Aceh"
      }
    ]
    }
  },
  methods: {
    nilai: function(){
      var jaw_1, jaw_2, jaw_3, jaw_4, jaw_5;

      if(this.picked1 == 'e'){ jaw_1 = 20; }else{ jaw_1 = 0;}
      if(this.picked2 == 'b'){ jaw_2 = 20; }else{ jaw_2 = 0;}
      if(this.picked3 == 'b'){ jaw_3 = 20; }else{ jaw_3 = 0;}
      if(this.picked4 == 'd'){ jaw_4 = 20; }else{ jaw_4 = 0;}
      if(this.picked5 == 'a'){ jaw_5 = 20; }else{ jaw_5 = 0;}

      return jaw_1 + jaw_2 + jaw_3 + jaw_4 + jaw_5;

    },
    jumlah_benar: function(){
      return this.nilai() / 20;
    },
    jumlah_salah: function(){
      return 5 - this.jumlah_benar() ;
    },
    hideTitle (){
    this.show = !this.show
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
button {
  background-color: lightgray;
  border-radius: 8px;
  border-color: darkgray;
  padding: 5px;
  padding-right: 15px; 
  padding-left: 15px;
  margin: 15px; 
}
table {
  font-family: Times New Roman;
}
hr {
  border-style: groove;
  height: 2px;
  width: 156.9%;
  margin-left: -246px;
}
</style>
