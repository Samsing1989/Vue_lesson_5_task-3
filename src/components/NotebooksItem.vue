<template>
  <div class="container">
    <div class="image"><img :src="notebooksCardData.imgSrc" /></div>

    <div class="body">
      <a :href="notebooksCardData.link" class="link-title">{{
        notebooksCardData.title
      }}</a>
      <div class="discount">
        Ваша економія <span>{{ notebooksCardData.discount }} ₴</span>
      </div>
      <div class="old-price">
        {{ notebooksCardData.oldPrice }} <span>₴</span>
      </div>
      <div class="price-link">
        <div class="price">{{ notebooksCardData.price }} <span>₴</span></div>
        <a :href="notebooksCardData.link" class="link">Купити</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NotebooksListItem",
  props: {
    notebooksCardData: {
      type: Object,
      default: () => ({}),
    },
  },
}
</script>

<style lang="css" scoped>
a {
  color: inherit;
  text-decoration: none;
}
.container {
  max-width: 650px;
  padding: 30px;
  display: flex;
  gap: 30px;
  border-bottom: 2px solid #b9b9b930;
}

.image img {
  width: 250px;
  height: 200px;
}

.link-title {
  display: block;
  font-size: 24px;
  color: rgb(31, 117, 238);
  margin-bottom: 10px;
}
.discount {
  margin-bottom: 15px;
}
.discount span {
  color: red;
}
.old-price {
  color: grey;
  text-decoration: line-through;
  margin-bottom: 5px;
}
.old-price span {
  font-size: 12px;
}
.price-link {
  display: flex;
  justify-content: space-between;
}
.price {
  font-size: 34px;
  color: red;
}
.price span {
  font-size: 16px;
}
.link {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: rgb(20, 177, 20);
  color: white;
  border-radius: 10px;
  transition: all 0.3s;
}
.link:hover {
  background-color: rgb(16, 125, 16);
}
</style>
