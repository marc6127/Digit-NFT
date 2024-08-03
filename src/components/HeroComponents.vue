<template>
    <section class="hero">
        <div class="textSection">
            <h1 class="title">See the NFT new world</h1>
            <div class="subTitle">
            <p class="description">Vorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eu turpis molestie, di</p>
            <div class="buttonSection">
            <p class="textButton">Discover Now</p>
            <img class="icon" src="../assets/arrowIcon.png" alt="arrowIcon" />
            </div>
            </div>
        </div>
        <div class="imageSection">
            <img class="imageUn" src="../assets/imageUn.png" alt="imageUn" />
            <img class="imageTrois" src="../assets/imageTrois.jpg" alt="imageTrois" />
            <img class="imageDeux" src="../assets/imageDeux.jpg" alt="imageDeux" />
        </div>
    </section>
  </template>
  
  <script>  
  
  export default {
    name: 'HeroComponents'
  }
  </script>
  
  <style>
    .hero {
      width: 1200px;
      height: 607px;
      display: flex;
    }
  
    .textSection {
      width: 757px;
      height: 390px;
    }
  
    .subTitle {
      margin-top: -70px;
    }
  
    .title {
      width: 787px;
      color: #181D28;
      font-weight: 400;
      font-size: 120px;
      line-height: 108px;
    }
  
    .description {
      width: 412px;
      height: 48px;
      color: #484D56;
      font-weight: 600;
      font-size: 16px;
      row-gap: 26px;
    }
  
    .buttonSection {
      widows: 165px;
      height: 48px;
      display: flex;
    }
  
    .textButton {
      color: #181D28;
      font-weight: 600;
      font-size: 16px;
      margin-right: 10px;
    }
  
    .icon {
      width: 48px;
      height: 48px;
    }
  
    .imageSection {
      width: 597px;
      height: 588px;
      margin-top: 100px;
      display: flex;
    }
  
    .imageUn {
      width: 157px;
      height: 116px;
      margin-top: 19px;
    }
  
    .imageDeux {
      width: 288px;
      height: 443px;
      border-radius: 184px;
    }
  
    .imageTrois {
      width: 288px;
      height: 443px;
      border-radius: 164px;
      margin-top: 145px;
      margin-right: 10px;
      margin-left: -300px;
    }
  </style>
  