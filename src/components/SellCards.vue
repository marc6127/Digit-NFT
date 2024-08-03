<template>
    <div class="card">
      <img class="cardIcon" :src="iconSrc" alt="Card icon">
      <div class="cardContent">
        <h2 class="cardTitle">{{ titleSell }}</h2>
        <p class="cardDescription">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc vulputate libero et velit interdum, ac aliquet odio mattis.</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'SellCards',
    props: {
      iconSrc: {
        type: String,
        required: true
      },
      titleSell: {
        type: String,
        required: true
      },
    }
  }
  </script>
  
  <style scoped>
  .card {
    width: 282px;
    height: auto;
    border-radius: 24px;
    background-color:#E8E9EA;
    padding: 24px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    align-items: start;
  }
  
  .cardIcon {
    width: 50px;
    height: 50px;
    border-radius: 8px;
    padding: 10px;
    gap: 10px;
    background-color: #181D28;
  }
  
  .cardContent {
    width: 100%;
    justify-content: space-between;
    align-items: start;
  }
  
  .cardTitle {
    font-size: 20px;
    font-weight: 700;
    line-height: 28px;
    color: #0E1218;
    margin: 0;
  }

  .cardDescription {
    font-size: 14px;
    font-weight: 500;
    line-height: 20px;
    color: #484D56;
    margin: 0;
  }
  </style>
  