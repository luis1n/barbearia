<template>
  <div class="card">
     <a href="item.href">
        <img :src="item.img" alt="Icone do servico"/>
        <span>{{ item.titulo }}</span>
     </a>
  </div>
</template>

<script>
export default {
    props:['item']
}
</script>

<style scoped>
div{
    margin: 20px 30px 20px 30px;
    display: block;
    width: 100px;
}
img{
    width: 80px;    
}
span{
    font-weight: 900;
    justify-content: center;
}
.card{
    background-color: rgba( 255, 255, 255, .5);
    display: flex ;
    justify-content: center;
    flex-direction: column;
    min-width: 80px;
    min-height: 150px;
    border: 1px solid grey;
    border-radius: 5%;
    opacity: .9;
    box-shadow: 0 0 2em grey;
    transition: box-shadow .5s;
}
</style>