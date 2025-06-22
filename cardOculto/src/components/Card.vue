<script>
export default {
  name: 'Card',

  data(){

  },
  methods :{
     complementosOcultar() {
        // variavel que eu butei pra pegar os elementos com o ref
        const el = this.$refs.complementos;

        if (el.style.display === 'none') {
        el.style.display = 'block'; // mostra
      } else {
        el.style.display = 'none'; // oculta
      }
    }
  }
}
 
</script>

<template>
    <div class="card">
      <h1>Card</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Enim iste nobis, earum unde repellat nemo quibusdam molestias reiciendis ea eaque fugit nulla animi ratione rem non obcaecati sunt magnam quo?
      </p>
      <img
        src="https://img.freepik.com/fotos-gratis/tigela-de-ceramica-de-deliciosa-sobremesa-brasileira-de-acai_23-2149788578.jpg?semt=ais_hybrid&w=740"
        alt="foto de açaí"
        class="img-card"/>

        <button @click="complementosOcultar">Mostrar Complementos</button>
        <div   ref="complementos">
            <ul>
                <li>xxxxxxx</li>
                <li>xxxxxxx</li>
                <li>xxxxxxx</li>
                <li>xxxxxxx</li>
                <li>xxxxxxx</li>
            </ul>
        </div>
    </div>
  </template>
  
  <style scoped>
  .card {
    border: 1px solid black;
    background-color: aqua;
    width: 400px;
    height: 80%;
    padding: 16px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
  }
  
  .img-card {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 8px;
  }
  </style>