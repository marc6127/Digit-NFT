<template>
  <div class="home">
    <NavbarComponents />
    <HeroComponents />
    <section class="collections">
      <h2 class="title">Our Collections</h2>
      <div class="buttonsAndLink">
        <div class="buttonCollections">
          <ButtonComponents
            v-for="(button, index) in buttons"
            :key="index"
            :classes="button.classes"
            :name="button.name"
          />
        </div>
        <a class="viewMore" href="#">View more</a>
      </div>
      <div class="cards">
        <CollectionsCards
          v-for="(card, index) in cards"
          :key="index"
          :imgSrc="card.imgSrc"
          :title="card.title"
        />
      </div>
    </section>
    <section class="sell">
      <h2 class="title">Create and Sell Now</h2>
      <div class="cards">
        <SellCards
          v-for="(sellCard, index) in sellCards"
          :key="index"
          :iconSrc="sellCard.iconSrc"
          :titleSell="sellCard.titleSell"
        />
      </div>
    </section>
    <section class="cta">
      <h2 class="titleCta">Build your NFT profile</h2>
      <p class="descriptionCta">Join almost 10k NFT profiles on Digit !</p>
      <div class="buttonCta">
        <ButtonComponents name="Sign up now" classes="btnCta"/>
      </div>
    </section>
    <footer>
        <img src="../assets/logo.png" alt="Logo" />
      <div class="linksFooter">
        <h3>Create Explore & Collect Digital  NFTs</h3>
        <div class="pages">
          <a href="">Privacy</a>
          <a href="">Terms & Conditions</a>
          <a href="">About Us</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import NavbarComponents from '@/components/NavbarComponents.vue';
import HeroComponents from '@/components/HeroComponents.vue';
import ButtonComponents from '@/components/ButtonComponents.vue';
import CollectionsCards from '@/components/CollectionsCards.vue';
import SellCards from '@/components/SellCards.vue';


//images des cards pour la section collection
import cardUn from '@/assets/cardUn.png';
import cardDeux from '@/assets/cardDeux.png';
import cardTrois from '@/assets/cardTrois.png';
import cardQuatre from '@/assets/cardQuatre.png';

//icone des cards pour la section sell et create
import iconUn from '@/assets/iconUn.png';
import iconDeux from '@/assets/iconDeux.png';
import iconTrois from '@/assets/iconTrois.png';
import iconQuatre from '@/assets/iconQuatre.png';

export default {
  name: 'HomeView',
  components: {
    NavbarComponents,
    HeroComponents,
    CollectionsCards,
    ButtonComponents,
    SellCards,
  },
  data() {
    return {
      buttons: [
        { name: 'All categories', classes: 'allCategories' },
        { name: 'Art', classes: 'art' },
        { name: 'Celebrities', classes: 'celebrities' },
        { name: 'Gaming', classes: 'gaming' },
        { name: 'Sport', classes: 'sport' },
      ],
      cards: [
        { imgSrc: cardUn, title: 'CyberPunk' },
        { imgSrc: cardDeux, title: 'Durolost  Boll - Upper' },
        { imgSrc: cardTrois, title: 'Space X Wiper' },
        { imgSrc: cardQuatre, title: 'Snoop Dogg' },
      ],
      sellCards: [
        { iconSrc: iconUn, titleSell: 'Set up your wallet' },
        { iconSrc: iconDeux, titleSell: 'Add your NFT’s' },
        { iconSrc: iconTrois, titleSell: 'Promote your NFT’s' },
        { iconSrc: iconQuatre, titleSell: 'Sell your NFT’s' },
      ],
    };
  },
};
</script>

<style>

/*Collections section*/

.collections {
  width: 1200px;
  height: 509px;
  margin-top: 150px;
}

.collections .title {
  width: 223px;
  color: #0e1218;
  font-weight: 700;
  font-size: 30px;
  line-height: 36px;
  margin-bottom: 20px;
}

.buttonsAndLink {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.buttonCollections {
  display: flex;
  gap: 8px;
}

.allCategories {
  background-color: #0e1218;
  width: auto;
  height: 40px;
  border-radius: 12px;
  padding: 10px 26px;
  font-weight: 600;
  font-size: 14px;
  line-height: 20px;
  color: white;
}

.art,
.celebrities,
.gaming,
.sport {
  background-color: #e8e9ea;
  width: auto;
  height: 40px;
  border: 0;
  border-radius: 12px;
  padding: 10px 26px;
  font-weight: 600;
  font-size: 14px;
  line-height: 20px;
  color: #0e1218;
}

.viewMore {
  font-weight: 600;
  font-size: 14px;
  line-height: 20px;
  color: #1a202c;
  text-decoration: none;
}

.cards {
  display: flex;
  width: 100%;
  height: auto;
  padding: 10px 0;
  gap: 24px;
}

/*Create et sell section*/

.sell {
  width: 1200px;
  height: 509px;
  margin-top: 100px;
}

.sell .title {
  font-weight: 700;
  font-size: 30px;
  line-height: 36px;
  color: #0E1218;
}

/** Call to action section */

.cta {
  position: relative;
  width: 1200px;
  height: 200px;
  border-radius: 32px;
  padding: 70px 0px;
  background-image: url("../assets/ctabg.png");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  opacity: 0.9;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center; 
}

.cta::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  border-radius: 32px;
  z-index: 1;
}

.cta > * {
  position: relative;
  z-index: 2;
}

.titleCta {
  text-align: center;
  color: white;
  font-weight: 500;
  font-size: 64px;
  line-height: 40px;
  margin: 0; 
}

.descriptionCta {
  text-align: center;
  color: white;
  font-weight: 600;
  font-size: 20px;
  line-height: 28px;
  margin: 10px 0; 
  padding-top: 20px;
}

.buttonCta {
  width: 146px;
  align-items: center;
  justify-content: center;
  border-radius: 42px;
  padding: 10px 26px;
  background-color: white;
  display: flex;
  align-items: center; 
  justify-content: center; 
  margin-top: 20px;
}
.btnCta {
  text-align: center;
  color: #0E1218;
  font-weight: 600;
  font-size: 16px;
  line-height: 24px;
  background: transparent;
  border: 0;
  width: 100%;
}

footer{
  width: 1200px;
  height: auto;
  margin-top: 100px;
}

.logo {
  width: 36px;
  height: 36px;
}

.linksFooter {
  display: flex;
  border: 0;
  border-top: 1px solid #B8BABE;
  justify-content: space-between;
  margin-top: 20px;
  padding: 15px 0px;
  align-items: center;
}

.linksFooter h3 {
  font-size: 24px;
  font-weight: 600;
  line-height: 32px;
  color: #181D28;
}

.pages a {
  font-size: 14px;
  font-weight: 500;
  line-height: 20px;
  margin-right: 20px;
  text-decoration: none;
  color: black;
}

</style>
