<template>
<div class="card">
<a :href="item.href">
  <div>
        <img :src="item.img" alt='Imagem do Link' />
        <span>{{ item.title }}</span>
  </div>
  </a>
  </div>
</template>

<script>
export default {
    props:['item']
}
</script>

<style scoped>
div {
    margin: 0px 15px 0px 15px;
    display: block;
    width: 100px;
}
img {
    width: 70px;
}
span {
    font-weight: 900;
}
.card {
    margin: 0px 20px 0px 20px;
    border: 1px solid grey;
    border-radius: 10%;
    min-width: 130px;
    min-height: 160px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    box-shadow: 0 0 1em grey;
}
.card:hover {
    background: rgba(45, 13, 226, 0.5);
}
</style>