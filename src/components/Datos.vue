
<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <div class="table-responsive">
          <table class="table">
            <thead class="table-dark">
              <tr>
                <th scope="col">ID</th>
                <th scope="col">Nombre</th>
                <th scope="col">Precio</th>
                <th scope="col">Stock</th>
                <th scope="col">Imagen</th>
              </tr>
            </thead>
            <tbody class="table table-dark table-striped">
              <tr v-for="item in items" :key="item.id">
                <th scope="row">{{ item.id }}</th>
                <td>{{ item.nombre }}</td>
                <td>{{ item.precio }}</td>
                <td>{{ item.stock }}</td>
                <td>{{ item.img }} {{ item.nombre }}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>


<script setup>
import { ref } from 'vue'
import datos from '../assets/postres.json'
import { computed } from 'vue'

defineProps: ['msg']

const items = ref(datos)



</script>  
