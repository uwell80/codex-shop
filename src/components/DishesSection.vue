<template>
  <section class="dishes" id="menu">
    <div class="section-heading" v-reveal>
      <div>
        <p class="section-kicker">SIGNATURE SELECTIONS</p>
        <h2>招牌涮品</h2>
      </div>
      <p>
        好食材不用复杂加工，<br />在滚烫锅底里，刚好七上八下。
      </p>
    </div>
    <div class="dish-grid">
      <article
        v-for="dish in dishes"
        :key="dish.no"
        class="dish-card"
        :class="{ 'dish-featured': dish.featured, 'dish-offset': dish.offset }"
        v-reveal="dish.delay"
      >
        <div class="dish-image">
          <img :src="dish.img" :alt="dish.alt" loading="lazy" decoding="async" />
        </div>
        <div class="dish-info">
          <p>{{ dish.no }}</p>
          <h3>{{ dish.name }}</h3>
          <span>{{ dish.price }}</span>
        </div>
      </article>
    </div>
    <a class="button button-outline" href="#reserve" v-reveal>查看涮品菜单 <b>↗</b></a>
  </section>
</template>

<script setup>
const dishes = [
  {
    no: 'SIGNATURE / 01',
    name: '吊龙 · 雪花肥牛拼盘',
    price: '¥ 128',
    img: 'https://img.freepik.com/premium-photo/raw-beef-slice-hot-pot-fresh-snowflake-beef-slices-chinese-food-selective-focus_479694-2697.jpg',
    alt: '精品牛肉拼盘',
    featured: true,
    offset: false,
    delay: '0ms',
  },
  {
    no: 'SIGNATURE / 02',
    name: '山野鲜蔬 · 竹荪拼盘',
    price: '¥ 58',
    img: 'https://images.unsplash.com/photo-1543339308-43e59d6b73a6?auto=format&fit=crop&w=900&q=85',
    alt: '山野鲜蔬拼盘',
    featured: false,
    offset: false,
    delay: '120ms',
  },
  {
    no: 'SIGNATURE / 03',
    name: '手打虾滑 · 蟹籽福袋',
    price: '¥ 52',
    img: 'https://jokia.com.sg/wp-content/uploads/2024/01/prawn-paste-ball.jpg',
    alt: '手打虾滑',
    featured: false,
    offset: true,
    delay: '240ms',
  },
]
</script>
