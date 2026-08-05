<script setup>
const dishes = [
  { name: '松露野菌手工宽面', description: '黑松露 / 牛肝菌 / 帕玛森', price: '¥66', imageClass: 'image-pasta', featured: true },
  { name: '柠香烤海鲈鱼', description: '时令蔬菜 / 茴香 / 青酱', price: '¥168', imageClass: 'image-fish', featured: false },
  { name: '焦糖无花果挞', description: '香草马斯卡彭 / 蜂蜜', price: '¥58', imageClass: 'image-dessert', featured: false },
]
</script>

<template>
  <section id="menu" class="menu-section">
    <div class="section-heading">
      <div><p class="eyebrow">A LITTLE TASTE OF TODAY</p><h2>今日餐桌</h2></div>
      <a class="text-link" href="#reserve">查看完整菜单 <span>→</span></a>
    </div>
    <div class="menu-grid">
      <article v-for="dish in dishes" :key="dish.name" class="dish" :class="{ 'dish-featured': dish.featured }">
        <div class="dish-image" :class="dish.imageClass"><span v-if="dish.featured">主厨推荐</span></div>
        <div class="dish-info"><div><h3>{{ dish.name }}</h3><p>{{ dish.description }}</p></div><b>{{ dish.price }}</b></div>
      </article>
    </div>
  </section>
</template>
