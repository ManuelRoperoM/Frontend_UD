<template>
  <header>
      <v-app-bar app class="customBar">
        <v-toolbar-title class="logo ml-12" v-if="windowWidth > 967">TORNEO UD</v-toolbar-title>
          <div class="btns mr-12" v-if="windowWidth > 967">
              <v-btn color="white" class="customBtn" @click="handleButtonClick">Home</v-btn>
              <v-btn color="white" class="customBtn" @click="handleButtonClick">Tabla</v-btn>
              <v-btn color="white" class="customBtn" @click="openDialog">Llamame</v-btn>
          </div>
      </v-app-bar>
    <DialogContactUs ref="dialogComponent"/>
  </header>
</template>

<script>
  import DialogContactUs from '~/components/Dialogs/DialogContactUs.vue';
  export default {
    components: {
      DialogContactUs,
    },
    data() {
      return {
        dialog: false,
        windowWidth: 0,
        items: [
          { title: 'Contactanos' },
          { title: 'Button 2' },
          { title: 'Button 3' },
          { title: 'Button 4' },
          { title: 'Button 5' },
          { title: 'Button 6' },
        ],
      };
    },
    methods: {
      handleButtonClick() {
        console.log('Botón clicado');
      },
      openDialog(){
        this.$refs.dialogComponent.openDialog();
      },
      handleMenuItemClick(item) {
        if (item.title === 'Contactanos') {
          this.openDialog();
        } else {
          // Puedes agregar lógica para otros elementos del menú aquí
          console.log(`Clic en ${item.title}`);
        }
      },
      updateWindowWidth() {
        this.windowWidth = window.innerWidth;
        console.log(this.windowWidth)
      },
      toggleMobileMenu() {
              this.mobileMenu = !this.mobileMenu;
      },
      },
    mounted() {
      window.addEventListener('resize', this.updateWindowWidth);
      this.updateWindowWidth();
      console.log("Holaa")
    },
    beforeDestroy() {
      window.removeEventListener('resize', this.updateWindowWidth);
    },
  }
</script>

<style scoped>
  .logo{
    color: gray;
    font-size: 3rem;
    font-weight: 1000;
    line-height: 1.5;
  }
  .customBtn{
    background-color: gray;
    margin-left: 10px;
    flex: 1;
    min-width: 103px;
  }  
  .v-dialog__content {
    z-index: 9999;
  }
  /* Diseño responsive */
  @media screen and (max-width: 1106px) {
    .logo {
      text-align: center;
      margin-top: 10px;
    }
    .customBtn {
      min-width: auto;
      margin-top: 10px;
      margin-bottom: 10px;
    }
  }

  @media screen and (max-width: 967px) {
    .customBar{
      height: 7.2rem;
    }
    .littleSize{
      width: 100%;
    }
    .logo{
      color: gray;
      font-size: 2.5rem;
      font-weight: 1000;
      line-height: 1.5;
      margin-top: 65px;
    }
    .customBtn {
      min-width: auto;
      margin-top: 2px;
    }
    .btns{
      width: 100% !important;
      display: flex;
      align-items: center;
      justify-content: center;
    }
  }
  @media screen and (max-width: 767px) {
    .customBar{
      height: 5.2rem;
      text-align: center;
    }
    .logo{
      color: gray;
      font-size: 2.5rem;
      font-weight: 1000;
      line-height: 1.5;
      margin-top: 20px;
      margin-bottom: 0px;
    }
    .burgerIcon{
      color: gray !important;
      margin-top: 0px;
      text-align: center;
      border-radius: 5%;
    }
    .listServices{
      text-align: center;
    }
  }
</style>