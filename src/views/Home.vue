<template>
  <div class="home">
    <navbar placeholder="¿Qué puedo encontrar para ti?"/>
    <div class="bg-amber-50" style="width: 100px; height: 100px">50</div>
    <div class="bg-amber-100" style="width: 100px; height: 100px">100</div>
    <div class="bg-amber-200" style="width: 100px; height: 100px">200</div>
    <div class="bg-amber-300" style="width: 100px; height: 100px">300</div>
    <div class="bg-amber-400" style="width: 100px; height: 100px">400</div>
    <div class="bg-amber-500" style="width: 100px; height: 100px">500</div>
    <div class="bg-amber-600" style="width: 100px; height: 100px">600</div>
    <div class="bg-amber-700" style="width: 100px; height: 100px">700</div>
    <div class="bg-amber-800" style="width: 100px; height: 100px">800</div>
    <div class="bg-amber-900" style="width: 100px; height: 100px">900</div>
  </div>
</template>

<script>
import navbar from './../components/Navbar';

export default {
  name: 'Home',
  components:{ navbar }
}
</script>
