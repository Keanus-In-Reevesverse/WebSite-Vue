<template>
    <header :class="{ 'scrolled-nav': scrollNav }">
        <nav>
            <div class="branding">
                <img src="../assets/logo.png" alt="Logo">
                <li>
                    <router-link class="link" :to="{ name: 'home' }">BuscaJogos+</router-link>
                </li>
            </div>
            <div v-show="!mobile" class="desk-navigation">
                <input type="search" class="header__search" placeholder=" O que procura ?">
                <div class="header__buttons">
                    <div v-if="!logged">
                        <!-- Login and registration buttons -->
                        <ul class="buttons-header">
                            <button @click="showLogin = true" type="button"
                                class="buttons-header__login">ENTRAR</button>
                            <q-dialog v-model="showLogin">
                               <Login/>
                            </q-dialog>
                            <button @click="showRegister = true" type="button"
                                class="buttons-header__registration">CADASTRAR</button>
                            <q-dialog v-model="showRegister">
                               <Register/>
                            </q-dialog>
                        </ul>
                    </div>
                    <div v-else>
                        <div class="q-pa-md">
                            <q-btn-dropdown label="Profile" dropdown-icon="change_history">
                                <q-list>
                                    <q-item clickable v-close-popup @click="">
                                        <q-item-section>
                                            <q-item-label>Favoritos</q-item-label>
                                        </q-item-section>
                                    </q-item>

                                    <q-item clickable v-close-popup @click="">
                                        <q-item-section>
                                            <q-item-label>Sair</q-item-label>
                                        </q-item-section>
                                    </q-item>
                                </q-list>
                            </q-btn-dropdown>
                        </div>
                    </div>
                </div>
            </div>
            <div class="icon">
                <i @click="toggleMobileNav" v-show="mobile" class="far fa-bars"
                    :class="{ 'icon-active': mobileNav }"></i>
            </div>
            <Transition name="mobile-container">
                <div v-show="mobileNav" class="mobile-navigation">
                    <input type="search" class="header__search" placeholder=" O que procura ?">
                    <div class="header__buttons">
                        <div v-if="!logged">
                            <!-- Login and registration buttons -->
                            <ul class="buttons-header">
                                <button @click="showLogin = true" type="button" class="buttons-header__login">ENTRAR</button>
                                <q-dialog v-model="showLogin">
                                    <Login/>
                                </q-dialog>
                                <button @click="showRegister = true" type="button" class="buttons-header__registration">CADASTRAR</button>
                                <q-dialog v-model="showRegister">
                                    <Register/>
                                </q-dialog>
                            </ul>
                        </div>
                        <div v-else>
                            <!-- layout sidebar mobile logado -->
                        </div>
                    </div>
                </div>
            </Transition>
        </nav>
    </header>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import { RouterLink } from 'vue-router'

import Register from './modal/ModalCadastro.vue'
import Login from './modal/ModalLogin.vue'

export default defineComponent({
    name: 'NavBar',
    components: {
        Register,
        Login,
    },
    setup() {
        return {
            showLogin: ref(false),
            showRegister: ref(false),
        }
    },
    data() {
        return {
            scrollNav: false,
            logged: false,
            mobile: true,
            mobileNav: false,
            windowWidth: 0,
        };
    },
    created() {
        window.addEventListener('resize', this.checkScreen);
        this.checkScreen();
    },
    mounted() {
        window.addEventListener('scroll', this.updateScroll);
    },
    methods: {
        updateScroll() {
            const scrollPosition = window.scrollY;
            if (scrollPosition > 50) {
                this.scrollNav = true;
                return;
            }
            this.scrollNav = false;
        },

        toggleMobileNav() {
            this.mobileNav = !this.mobileNav;
        },

        checkScreen() {
            this.windowWidth = window.innerWidth;
            if (this.windowWidth <= 790) {
                this.mobile = true;
                return;
            }
            this.mobile = false;
            this.mobileNav = false;
            return;
        },
    },
})
</script>

<style lang="scss" scoped>
header {
    background-color: rgb(0, 0, 0);
    z-index: 999;
    width: 100%;
    position: fixed;
    transition: 0.5s ease all;

    nav {
        position: relative;
        display: flex;
        flex-direction: row;
        padding: 1rem 0;
        transition: 0.5s ease all;
        width: 90%;
        margin: 0 auto;

        @media(min-width: 78rem) {
            max-width: 78rem;
        }

        ul,
        .link {
            font-weight: 500;
            font-family: var(--main-font);
            color: var(--background-color-dark-white);
            list-style: none;
            text-decoration: none;
        }

        li {
            text-transform: uppercase;
            padding: 1.2rem;
            margin-left: 1.2rem;
        }

        .link {
            font-size: 16px;
            transition: 0.5s ease all;
            padding-bottom: 4px;
            border-bottom: 1px solid transparent;

            &:hover {
                color: #00afea;
                border-color: #00afea;
            }
        }

        .branding {
            display: flex;
            align-items: center;

            img {
                width: 3.2rem;
                transition: 0.5s ease all;
            }
        }

        .desk-navigation {

            display: flex;
            align-items: center;
            flex: 1;
            justify-content: flex-end;
        }

        .header__search {
            margin-right: 1.5em;
            background-color: transparent;
            border: 2px solid var(--gray);
            color: var(--background-color-white);
            border-radius: 24px;
            padding: 0.75em;
            width: 21.5rem;
        }

        .header__search:hover {
            transform: scale(1.10);
            border: 2px solid var(--background-color-white);
        }

        .header__search::placeholder {
            font-family: var(--main-font);
            font-size: 16px;
            font-weight: 700;
            text-align: center;
            justify-content: space-between;
            color: var(--background-color-white);
            background: url(../assets/Pesquisa.svg) no-repeat;
            background-position: 1em;
        }

        /*CSS Login and registration buttons*/
        .buttons-header {
            padding: 0 2em;
            justify-content: space-between;
            display: flex;
        }

        .buttons-header__login,
        .buttons-header__registration {
            font-family: var(--main-font);
            font-size: 16px;
            font-weight: 700;
            color: var(--ligth-green);
            border-radius: 10px;
            padding: 0.5em;
            background-color: transparent;
            border: 2px solid var(--ligth-green);
        }

        .buttons-header__login:hover,
        .buttons-header__registration:hover {
            color: var(--dark-green);
            border: 2px solid var(--dark-green);
            transform: scale(1.10)
        }

        .buttons-header__login {
            margin-right: 1em;
        }

        .icon {
            display: flex;
            align-items: center;
            position: absolute;
            top: 0;
            right: 1.5rem;
            height: 100%;

            i {
                cursor: pointer;
                font-size: 1.5rem;
                color: #fff;
                transition: 0.5s ease all;
            }
        }

        .icon-active {
            transform: rotate(180deg);
        }

        .mobile-navigation {
            display: flex;
            flex-direction: column;
            align-items: center;
            position: fixed;
            width: 100%;
            max-width: 15.62rem;
            height: 100%;
            background: var(--background-color-dark-white);
            top: 0;
            left: 0;

            .header__search {
                margin-top: 1.25rem;
                margin-bottom: 1.25rem;
                width: 12rem;
                color: #000;
                justify-items: center;

            }

            .header__search::placeholder {
                color: black;
                background: url(../assets/Pesquisa.svg) no-repeat;

            }

        }

        .mobile-container-enter-active,
        .mobile-container-leave-active {
            transition: 0.8s ease all;
        }

        .mobile-container-enter-from,
        .mobile-container-leave-to {
            transform: translateX(-15.62rem);
        }

        .mobile-container-enter-to {
            transform: translateX(0);
        }
    }
}

.scrolled-nav {
    background-color: #000;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);

    nav {
        padding: 8px 0;

        .branding {
            img {
                width: 2.5rem;
                box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            }
        }
    }

}
</style>

