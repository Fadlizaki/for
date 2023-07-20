<script setup>
import { ref } from "vue";
let kata = "dunia ada cerita";
let name = "<h1> nama saya fadli </h1>";
let pesan = "lihat ke bawah !!!"
let satu = 10
let dua = 10

let massage = ref("hai vue js");
function balikkata() {
  massage.value = massage.value.split('').reverse('').join('')
}
</script>

<template>
  <div>
    <span>{{ kata }}</span> <br>
    <span style="color: red">Ini seharusnya merah.</span>
    <span v-html="name"></span>
    <span v-html="pesan"></span> <br>
    <h2 v-if="satu > dua">goblok</h2>
    <h1 v-else-if="dua > satu"> bener nih</h1>
    <h3 v-else>tolol</h3>
    <button v-bind:disabled="isButtonDisabled">Tombol</button>

    <!-- split button -->
    <p>{{ massage }}</p>
    <button v-on:click="balikkata">balikan kata</button>

    <!-- For -->
    <br>
    pengulangan
    <ol>
      <li v-for="todo in todos">
        {{ todo.teks }}
      </li>
    </ol>

    <!-- input -->
    <p>
      {{ pesan }}
    </p>
  </div>
</template>

