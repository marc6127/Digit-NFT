<template>
  <div class="card">
    <img class="cardImg" :src="imgSrc" alt="Card image">
    <div class="cardContent">
      <h2 class="cardTitle">{{ title }}</h2>
      <div class="cardPrice">
        <img class="cardIcon" src="../assets/cardIcon.jpg" alt="Card icon">
        <p class="price">68</p>
      </div>
    </div>
    <button class="cardButton">Place a Bid</button>
  </div>
</template>

<script>
export default {
  name: 'CollectionsCards',
  props: {
    imgSrc: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.card {
  width: 282px;
  height: 341px;
  border-radius: 20px;
  border: 1px solid #B8BABE;
  padding: 12px;
  display: flex;
  flex-direction: column;
  gap: 16px;
  align-items: center;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.cardImg {
  width: 100%;
  height: 213px;
  border-radius: 20px;
  object-fit: cover;
}

.cardContent {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.cardTitle {
  font-size: 16px;
  font-weight: 700;
  line-height: 24px;
  margin: 0;
}

.cardPrice {
  display: flex;
  align-items: center;
  gap: 8px;
}

.cardIcon {
  width: 24px;
  height: 24px;
}

.price {
  font-size: 18px;
  font-weight: 700;
  line-height: 28px;
  margin: 0;
}

.cardButton {
  width: 100%;
  border: 1px solid #0E1218;
  padding: 10px 0;
  border-radius: 12px;
  font-size: 16px;
  font-weight: 600;
  line-height: 24px;
  background-color: white;
  cursor: pointer;
  transition: background-color 0.3s ease, color 0.3s ease;
}

.cardButton:hover {
  background-color: #0E1218;
  color: white;
}
</style>
