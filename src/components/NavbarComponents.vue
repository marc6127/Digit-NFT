<template>
  <nav v-if="isDesktop">
    <div class="logo">
      <img src="../assets/logo.png" alt="Logo" />
    </div> 
    <div class="menu">
        <ul>
            <li v-for="(item, index) in links" :key="index">{{ item }}</li>
        </ul>
    </div>
    <div class="button">
      <ButtonComponents name="Sign up" classes="register"/>
      <ButtonComponents name="Connect Wallet" classes="login"/>
    </div>
  </nav>
 <!-- <nav v-if="isTablet">
    <div class="logo">
      <img src="../assets/logo.png" alt="Logo" />
    </div>
    <button @click="toggleSidebar" class="menuIcon">☰</button>
    <div v-if="showSidebar" class="sidebar">
      <ul>
        <li v-for="(item, index) in links" :key="index">{{ item }}</li>
      </ul>
      <button @click="toggleSidebar" class="close-icon">X</button>
    </div>
  </nav> -->
</template>

<script>
import ButtonComponents from '@/components/ButtonComponents.vue'
export default {
  name: "NavbarComponents",
  components: {
    ButtonComponents,
  },
  data() {
    return {
      links: ['Home', 'Top sales', 'Collections', 'Our blog', 'About us'],
      isDesktop: window.innerWidth >= 1200,
      isTablet: window.innerWidth >= 768
    };
  },
};
</script>

<style>
/* Desktop navbar */
nav {
  width: 1200px;
  display: flex;
  justify-content: space-between;
  padding: 16px 0;
  align-items: center;
}

.logo {
  width: 36px;
  height: 36px;
}

.menu {
  width: 460px; 
  height: 24px;
}

ul {
  list-style-type: none;
  justify-content: center;
  align-items: center;
  display: flex;
  gap: 28px;
  padding: 0;
  margin: 0;
}

li {
  font-family: "Raleway";
  font-weight: 600;
  font-size: 16px;
  color: #12171F;
  word-wrap: break-word;
}

.button {
  width: 400px;
  height: 44px;
  display: flex;
  align-items: center;
  justify-content: end;
  gap: 20px;
}

.register {
  width: 150px;
  height: 100%;
  border: 0;
  border-right: 2px solid #0E1218;
  padding: 4px 26px; 
  background-color: transparent;
  color: #0E1218;
  font-size: 16px;
  font-weight: 600;
  line-height: 24px;
  word-wrap: break-word;

}

.login {
  width: 180px;
  height: 100%;
  border-radius: 42px;
  padding: 10px 26px; 
  background-color: #0E1218;
  color: white;
  font-size: 16px;
  font-weight: 600;
  line-height: 24px;
  word-wrap: break-word;
}

/* Tablet navbar */
@media (width >= 768px) {
 /* nav {
    width: 676px;
    top: 12px;
    left: 120px;
    display: flex;
    justify-content: space-between;
    position: fixed;
    padding: 16px 0;
    align-items: center;
  }

  .menuIcon {
    width: 30px;
    height: 30px;
    border: solid 1.3px #0B0D12;
    border-radius: 8px;
    justify-content: space-between;
    padding: 8px;
    background-color: transparent;
    font-weight: 900;
  }

  .logo {
    width: 36px;
    height: 36px;
  }*/
}
</style>
