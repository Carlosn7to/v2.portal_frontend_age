<script setup lang="ts">

import { RouterLink } from "vue-router";

import { stateMenu } from "@/stores/counter";
import {ref} from "vue";


const alterStateMenu = () => {
  stateMenu().alternateState(!stateMenu().status);
}

const actualMenu = ref('commission');
const actualSubMenu = ref('')

</script>

<template>
  <div class="menu__container" :class="{'retract' : stateMenu().status}">
    <button @click="alterStateMenu">
      <svg v-if="stateMenu().status" xmlns="http://www.w3.org/2000/svg" id="arrow-circle-down" viewBox="0 0 24 24" width="512" height="512"><path d="M0,12A12,12,0,1,0,12,0,12.013,12.013,0,0,0,0,12Zm16,0a2.993,2.993,0,0,1-.752,1.987c-.291.327-.574.637-.777.84L11.647,17.7a1,1,0,1,1-1.426-1.4L13.05,13.42c.187-.188.441-.468.7-.759a1,1,0,0,0,0-1.323c-.258-.29-.512-.57-.693-.752L10.221,7.7a1,1,0,1,1,1.426-1.4l2.829,2.879c.2.2.48.507.769.833A2.99,2.99,0,0,1,16,12Z"/></svg>
      <svg v-else xmlns="http://www.w3.org/2000/svg" id="arrow-circle-down" viewBox="0 0 24 24" width="512" height="512"><path d="M24,12A12,12,0,1,0,12,24,12.013,12.013,0,0,0,24,12ZM8,12a2.993,2.993,0,0,1,.752-1.987c.291-.327.574-.637.777-.84L12.353,6.3a1,1,0,0,1,1.426,1.4L10.95,10.58c-.187.188-.441.468-.7.759a1,1,0,0,0,0,1.323c.258.29.512.57.693.752L13.779,16.3a1,1,0,0,1-1.426,1.4L9.524,14.822c-.2-.2-.48-.507-.769-.833A2.99,2.99,0,0,1,8,12Z"/></svg>
    </button>
   <div class="content__menu">
     <div class="header__menu" >
       <div class="logo__header">
         <img src="@/assets/img/company/logo_orange.png" alt="logo" />
         <h1>Age</h1>
       </div>
     </div>
     <div class="items__menu">
       <div class="wrapper__menu">
         <span class="title__wrapper">Menu</span>
         <nav>
           <ul class="list__menu">
<!--             <li class="item__menu">-->
<!--               <router-link to="/inicio" :class="{'active__link' : actualMenu == 'home'}" @click="actualMenu = 'home'">-->
<!--                 <div class="active__item">-->
<!--                 </div>-->
<!--                 <svg xmlns="http://www.w3.org/2000/svg" id="Layer_1" data-name="Layer 1" viewBox="0 0 24 24" width="512" height="512"><path d="M14,18h-4c-1.103,0-2-.897-2-2v-4c0-1.103,.897-2,2-2h4c1.103,0,2,.897,2,2v4c0,1.103-.897,2-2,2Zm-4-6v4h4.002l-.002-4h-4Zm9,12H5c-2.757,0-5-2.243-5-5V9.724c0-1.665,.824-3.215,2.204-4.145L9.203,.855c1.699-1.146,3.895-1.146,5.594,0l7,4.724c1.379,.93,2.203,2.479,2.203,4.145v9.276c0,2.757-2.243,5-5,5ZM12,1.997c-.584,0-1.168,.172-1.678,.517L3.322,7.237c-.828,.558-1.322,1.487-1.322,2.486v9.276c0,1.654,1.346,3,3,3h14c1.654,0,3-1.346,3-3V9.724c0-.999-.494-1.929-1.321-2.486L13.678,2.514c-.51-.345-1.094-.517-1.678-.517Z"/></svg>-->
<!--                 <span>Início</span>-->
<!--               </router-link>-->
<!--             </li>-->
             <li class="item__menu">
               <router-link to="/ageCommissiona/b2b/financeiro" :class="{'active__link' : actualMenu == 'commission'}" @click="actualMenu = 'commission'">
                 <svg xmlns="http://www.w3.org/2000/svg" id="Layer_1" data-name="Layer 1" viewBox="0 0 24 24" width="512" height="512"><path d="M8,3.62c0-1.45,1.18-2.62,2.62-2.62h.38c0-.55,.45-1,1-1s1,.45,1,1h.27c1.07,0,2.06,.57,2.6,1.5,.28,.48,.11,1.09-.36,1.37-.48,.28-1.09,.11-1.37-.36-.18-.31-.51-.5-.87-.5h-2.64c-.34,0-.62,.28-.62,.62,0,.31,.22,.57,.52,.62l3.28,.55c1.27,.21,2.19,1.3,2.19,2.59,0,1.45-1.18,2.62-2.62,2.62h-.38c0,.55-.45,1-1,1s-1-.45-1-1h-.27c-1.07,0-2.06-.57-2.6-1.5-.28-.48-.11-1.09,.36-1.37,.48-.28,1.09-.11,1.37,.36,.18,.31,.51,.5,.87,.5h2.64c.34,0,.62-.28,.62-.62,0-.31-.22-.57-.52-.62l-3.28-.55c-1.27-.21-2.19-1.3-2.19-2.59Zm12.4-.57c-1.42,.28-2.4,1.61-2.4,3.06v5.05c-.26-.09-.54-.15-.83-.17-.79-.04-1.57,.23-2.17,.77l-3,2.76c-.08-.08-.17-.17-.25-.25l-2.74-2.52c-.6-.54-1.38-.81-2.16-.76-.29,.02-.57,.07-.83,.17V6c0-1.85-1.68-3.31-3.6-2.94-1.42,.28-2.4,1.61-2.4,3.06v9.98c0,2.12,.84,4.16,2.34,5.66l1.95,1.95c.2,.2,.45,.29,.71,.29s.51-.1,.71-.29c.39-.39,.39-1.02,0-1.41l-1.95-1.95c-1.13-1.13-1.76-2.65-1.76-4.24V6c0-.55,.45-1,1-1s1,.45,1,1c0,0,0,8.13,.02,8.19,.04,.63,.28,1.26,.73,1.78l2.62,2.72c.38,.4,1.01,.41,1.41,.03,.4-.38,.41-1.02,.03-1.41l-2.57-2.67c-.32-.38-.31-.94,.02-1.31,.18-.2,.42-.32,.69-.33,.27-.01,.52,.08,.71,.25l2.73,2.52c1.03,.95,1.61,2.28,1.61,3.68v3.56c0,.55,.45,1,1,1s1-.45,1-1v-3.56c0-1.15-.29-2.28-.82-3.28l3.07-2.87c.39-.36,.98-.36,1.38-.01,.43,.39,.45,1.05,.05,1.46l-2.4,2.48c-.38,.4-.37,1.03,.03,1.41,.19,.19,.44,.28,.69,.28,.26,0,.52-.1,.72-.31l2.58-2.68c.44-.52,.67-1.16,.69-1.8,0-.04,0-8.12,0-8.12,0-.55,.45-1,1-1s1,.45,1,1v10.1c0,1.59-.63,3.12-1.76,4.24l-1.95,1.95c-.39,.39-.39,1.02,0,1.41,.2,.2,.45,.29,.71,.29s.51-.1,.71-.29l1.95-1.95c1.5-1.5,2.34-3.53,2.34-5.66V6c0-1.85-1.68-3.31-3.6-2.94Z"/></svg>
                 <span>Comissão</span>
               </router-link>
             </li>

<!--             <li class="item__menu">-->
<!--                <div class="title__submenu" :class="{'active__group' : actualMenu == 'management'}">-->
<!--                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="512" height="512"><g id="_01_align_center" data-name="01 align center"><path d="M10.931,2.75a3.728,3.728,0,0,0-7.195,0H0v2H3.736a3.728,3.728,0,0,0,7.195,0H24v-2ZM7.333,5.5a1.75,1.75,0,1,1,1.75-1.75A1.753,1.753,0,0,1,7.333,5.5Z"/><path d="M16.667,8.25A3.745,3.745,0,0,0,13.07,11H0v2H13.07a3.727,3.727,0,0,0,7.194,0H24V11H20.264A3.745,3.745,0,0,0,16.667,8.25Zm0,5.5A1.75,1.75,0,1,1,18.417,12,1.752,1.752,0,0,1,16.667,13.75Z"/><path d="M7.333,16.5a3.745,3.745,0,0,0-3.6,2.75H0v2H3.736a3.728,3.728,0,0,0,7.195,0H24v-2H10.931A3.745,3.745,0,0,0,7.333,16.5Zm0,5.5a1.75,1.75,0,1,1,1.75-1.75A1.753,1.753,0,0,1,7.333,22Z"/></g></svg>-->
<!--                  <span>Gerenciamento</span>-->
<!--                  <svg v-if="actualMenu != 'management'" @click="actualMenu = 'management'" xmlns="http://www.w3.org/2000/svg" id="Outline" viewBox="0 0 24 24" width="512" height="512"><path d="M15.4,9.88,10.81,5.29a1,1,0,0,0-1.41,0,1,1,0,0,0,0,1.42L14,11.29a1,1,0,0,1,0,1.42L9.4,17.29a1,1,0,0,0,1.41,1.42l4.59-4.59A3,3,0,0,0,15.4,9.88Z"/></svg>-->
<!--                  <svg v-else @click="[actualMenu = '', actualSubMenu = '']" xmlns="http://www.w3.org/2000/svg" id="Outline" viewBox="0 0 24 24" width="512" height="512"><path d="M18.71,8.21a1,1,0,0,0-1.42,0l-4.58,4.58a1,1,0,0,1-1.42,0L6.71,8.21a1,1,0,0,0-1.42,0,1,1,0,0,0,0,1.41l4.59,4.59a3,3,0,0,0,4.24,0l4.59-4.59A1,1,0,0,0,18.71,8.21Z"/></svg>-->
<!--                </div>-->
<!--                  <transition name="fade">-->
<!--                    <ul class="list__submenu" v-if="actualMenu == 'management'">-->
<!--                      <li class="item__submenu" :class="{'active__submenu' : actualSubMenu == 'users'}" @click="actualSubMenu = 'users'">-->
<!--                        <p>Usuários</p>-->
<!--                      </li>-->
<!--                      <li class="item__submenu" :class="{'active__submenu' : actualSubMenu == 'permissions'}" @click="actualSubMenu = 'permissions'">-->
<!--                        <p>Permissões</p>-->
<!--                      </li>-->
<!--                      <li class="item__submenu" :class="{'active__submenu' : actualSubMenu == 'settings'}" @click="actualSubMenu = 'settings'">-->
<!--                        <p>Configurações</p>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </transition>-->
<!--             </li>-->
           </ul>
         </nav>
       </div>
       <div class="wrapper__menu" style="margin-top: auto">
         <span class="title__wrapper">Conta</span>
         <nav>
           <ul class="list__menu">
             <li class="item__menu">
               <router-link to="/perfil" :class="{'active__link' : actualMenu == 'account'}" @click="actualMenu = 'account'">
                 <svg xmlns="http://www.w3.org/2000/svg" id="Layer_1" data-name="Layer 1" viewBox="0 0 24 24" width="512" height="512"><path d="M9,12c3.309,0,6-2.691,6-6S12.309,0,9,0,3,2.691,3,6s2.691,6,6,6Zm0-10c2.206,0,4,1.794,4,4s-1.794,4-4,4-4-1.794-4-4,1.794-4,4-4Zm1.75,14.22c-.568-.146-1.157-.22-1.75-.22-3.86,0-7,3.14-7,7,0,.552-.448,1-1,1s-1-.448-1-1c0-4.962,4.038-9,9-9,.762,0,1.519,.095,2.25,.284,.535,.138,.856,.683,.719,1.218-.137,.535-.68,.856-1.218,.719Zm12.371-4.341c-1.134-1.134-3.11-1.134-4.243,0l-6.707,6.707c-.755,.755-1.172,1.76-1.172,2.829v1.586c0,.552,.448,1,1,1h1.586c1.069,0,2.073-.417,2.828-1.172l6.707-6.707c.567-.567,.879-1.32,.879-2.122s-.312-1.555-.878-2.121Zm-1.415,2.828l-6.708,6.707c-.377,.378-.879,.586-1.414,.586h-.586v-.586c0-.534,.208-1.036,.586-1.414l6.708-6.707c.377-.378,1.036-.378,1.414,0,.189,.188,.293,.439,.293,.707s-.104,.518-.293,.707Z"/></svg>
                 <span>Perfil</span>
               </router-link>
             </li>
             <li class="item__menu">
               <router-link to="/">
                 <svg xmlns="http://www.w3.org/2000/svg" id="Outline" viewBox="0 0 24 24" width="512" height="512"><path d="M22.829,9.172,18.95,5.293a1,1,0,0,0-1.414,1.414l3.879,3.879a2.057,2.057,0,0,1,.3.39c-.015,0-.027-.008-.042-.008h0L5.989,11a1,1,0,0,0,0,2h0l15.678-.032c.028,0,.051-.014.078-.016a2,2,0,0,1-.334.462l-3.879,3.879a1,1,0,1,0,1.414,1.414l3.879-3.879a4,4,0,0,0,0-5.656Z"/><path d="M7,22H5a3,3,0,0,1-3-3V5A3,3,0,0,1,5,2H7A1,1,0,0,0,7,0H5A5.006,5.006,0,0,0,0,5V19a5.006,5.006,0,0,0,5,5H7a1,1,0,0,0,0-2Z"/></svg>
                 <span>Sair</span>
               </router-link>
             </li>
           </ul>
         </nav>
       </div>

     </div>

   </div>

  </div>
</template>

<style scoped lang="scss">
.menu__container {
  width: 15%;
  height: 100%;
  background-color: #ffffff;
  padding: 3vh 0;
  position: relative;
  transition: all .3s ease-in-out;
  @include flex(column, flex-start, initial);
  box-shadow: $global-box-shadow;

  button {
    border: none;
    outline: none;
    position: absolute;
    top: 10%;
    right: -1.3vw;
    z-index: 3;
    background-color: transparent;

    svg {
      width: 1.5vw;
      height: 1.5vw;
      fill: #42A6DF;
      cursor: pointer;
      transition: opacity .3s ease-in-out;
      &:hover {
        opacity: .9;
      }
    }
  }

  .content__menu {
    @include flex(column, flex-start, initial);
    @include container(100%, 100%);
    overflow: hidden;
    padding: 1vh 0;

    .header__menu {
      @include flex(row, flex-start, center);
      height: 6vh;
      padding: 0 1vw;

      .logo__header {
        @include flex(row, flex-start, center, .5vw);

        img {
          width: 3vw;
          height: auto;
          transition: width .3s ease-in-out;
        }

        h1 {
          font-size: 2.4rem;
          font-weight: 500;
          color: #333;
          transition: opacity .3s ease-in-out;
        }
      }


    }

    .items__menu {
      padding: 3vh 1vw;
      height: 100%;
      @include flex(column, flex-start, intial, 1vh);

      .title__wrapper {
        font-size: 1.2rem;
        font-weight: 500;
        color: #535353;
        margin-bottom: 2vh;

      }

      nav {
        .list__menu {
          @include flex(column, flex-start, initial);
          list-style-type: none;
          padding: 0;

          .item__menu {
            padding: .5vh .2vw;

            a {
              background-color: #ffffff;
              width: 100%;
              padding: 7px 7px;
              border-radius: 5px;
              @include flex(row, flex-start, center, .5vw);
              position: relative;
              transition: background-color .3s ease-in-out, box-shadow .3s ease-in-out;

              .active__item {
                width: 30px;
                height: 45px;
                background-color: #53AEE2;
                position: absolute;
                left: -30%;
                top: -17%;
                border-radius: 50%;
              }

              svg {
                width: 1.4rem;
                height: auto;
                fill: #222;
              }

              span {
                font-size: 1.2rem;
                color: #222;
                font-weight: 500;
              }

              &:hover {
                background-color: #EEEEEE;
                box-shadow: $global-box-shadow;
              }
            }

            .active__link {
              background-color: #EEEEEE;
              box-shadow: $global-box-shadow;

              .active__item {
                animation: active__item__animation .3s ease-in-out forwards;
              }

              @keyframes active__item__animation {
                from {
                  left: -30%;
                }
                to {
                  left: -24%;
                }
              }

              &:hover {
                background-color: #e7e7e7;
              }
            }

            .active__group {
              background-color: #EEEEEE;
              box-shadow: $global-box-shadow;
              border-radius: 5px;

              &:hover {
                background-color: #e7e7e7;
              }
            }

            .title__submenu {
              width: 100%;
              padding: 7px 7px;
              @include flex(row, flex-start, center, .5vw);
              transition: all .3s ease-in-out;

              span {
                font-size: 1.2rem;
                color: #222;
                font-weight: 500;
              }

              svg {
                width: 1.4rem;
                height: auto;
                fill: #222;
              }

              svg:last-child {
                margin-left: auto;
                cursor: pointer;
                width: 1.6rem;
              }

            }

            .list__submenu {
              list-style-type: none;
              padding: 2vh 0 1vh 0;
              margin-left: 1vw;
              position: relative;

              &::before {
                content: ""; /* Necessário para gerar o pseudo-elemento */
                position: absolute;
                top: 1vh; /* Alinha o pseudo-elemento na parte inferior do elemento pai */
                left: -1px; /* Começa do lado esquerdo do elemento pai */
                width: 1%; /* Define a largura do pseudo-elemento como 20% do elemento pai */
                border-left: 1px solid #cccccc;
                height: 68%;
              }

              .item__submenu {
                padding: 1vh 0 1vh 1.5vw;
                border-bottom: 1px solid transparent; /* Opcional, se você quiser manter um guia de borda */
                border-radius: 10px;
                font-size: 1.2rem;
                color: #666;
                font-weight: 400;
                position: relative;

                p {
                  cursor: pointer;
                  border-radius: 5px;
                  padding: 5px 5px;
                  transition: all .3s ease-in-out;

                  &:hover {
                    background-color: #EEEEEE;
                    box-shadow: $global-box-shadow;
                  }

                }

                &::before {
                  content: ""; /* Necessário para gerar o pseudo-elemento */
                  position: absolute;
                  top: 0; /* Alinha o pseudo-elemento na parte inferior do elemento pai */
                  left: -1px; /* Começa do lado esquerdo do elemento pai */
                  width: 10%; /* Define a largura do pseudo-elemento como 20% do elemento pai */
                  border-bottom: 1px solid #cccccc; /* Estiliza a borda como desejado */
                  border-left: 1px solid #cccccc;
                  height: 50%;
                  border-radius: 0 0 0 3px;
                }
              }

              .item__submenu:last-child::before {
                content: ""; /* Necessário para gerar o pseudo-elemento */
                position: absolute;
                top: 0; /* Alinha o pseudo-elemento na parte inferior do elemento pai */
                left: -1px; /* Começa do lado esquerdo do elemento pai */
                width: 10%; /* Define a largura do pseudo-elemento como 20% do elemento pai */
                border-bottom: 1px solid #cccccc; /* Estiliza a borda como desejado */
                border-left: 1px solid #cccccc;
                height: 50%;
                border-radius: 0 0 0 10px;
              }

              .active__submenu {
                p {
                  background-color: #EEEEEE;
                  box-shadow: $global-box-shadow;

                  &:hover {
                    background-color: #e7e7e7;
                  }
                }
              }

            }
          }
        }
      }
    }
  }

  .alternate_menu__header {
    position: absolute;
    top: 5vh;
    right: -1vw;

    button {
      border: none;
      outline: none;
      border-radius: 50%;
      background-color: #f5f5f5;
      width: 2vw;
      height: 2vw;
      cursor: pointer;
    }
  }
}

.retract {
  width: 5%;

  

  h1, span, .active__item, .title__submenu > svg:last-child {
    opacity: 0;
    display: none;
  }

  a, .title__submenu {
    justify-content: center !important;
  }

  .title__submenu {
    &:hover {
      background-color: #EEEEEE;
      box-shadow: $global-box-shadow;
      border-radius: 5px;
      cursor: pointer;
    }
  }



}

@keyframes retract-menu {
  from {
    opacity: 1;
    display: block;
  }
  to {
    opacity: 0;
    display: none;
  }
}


.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

</style>