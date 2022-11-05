<template>
    <div id="modalRegister" class="modalOverlay">
        <div class="modal">
            <a href="#" class="close">&times;</a>
            <div class="content">
                <div class="form-container">
                    <h3 class="title">Cadastro</h3>
                    <form action="" class="form-horizontal">
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Insira o nome de usuário">
                        </div>

                        <div class="form-group">
                            <input type="email" class="form-control" placeholder="Insira o email">
                        </div>

                        <div class="form-group">
                            <input type="email" class="form-control" placeholder="Confirme o email">
                        </div>

                        <div class="form-group">
                            <input type="tel" class="form-control" placeholder="Insira o número de celular (Opcional)">
                        </div>

                        <div class="form-group">
                            <input type="password" class="form-control" placeholder="Insira a senha">
                        </div>

                        <div class="form-group">
                            <input type="password" class="form-control" placeholder="Confirme a senha">
                        </div>
                        <button class="btn">Cadastrar</button>
                    </form>
                    <label class="user-singup">
                        <a href="modallogin.html">Ja possui uma conta?</a>
                    </label>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'ModalCastro'
})

</script>

<style lang="scss">
@import url('../../styles/css/modalBase.css');

body {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: black;
}

.button {
    position: fixed;
    top: 288px;
    left: -3.56rem;
    letter-spacing: 1px;
    margin: 0 auto 0;
    display: block;
    z-index: 99;
    -ms-transform: rotate(270deg);
    transform: rotate(270deg);
    border-radius: 3px;
    font-family: 'Raleway', sans-serif;
    padding: 16px 20px;
    text-decoration: none;
    background-color: #fff;
    color: #007bb0;
    font-weight: 500;
    box-shadow: 0 0 15px rgb(0 0 0 / 30%);
    font-size: 22px;
}

.button:hover {
    background-color: #007bb0;
    color: #fff;
}

.modalOverlay {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background: #007bb0;
    transition: opacity 500ms;
    visibility: hidden;
    opacity: 0;
}

.modalOverlay:target {
    visibility: visible;
    opacity: 1;
}

.modal {
    margin: 4.37rem auto;
    padding: 1.3rem;
    background: #fff;
    border-radius: 10px;
    width: 25%;
    position: relative;
    box-shadow: 10px 7px 5px rgba(0, 0, 0, 0.290);
}

@media(max-width:992px) {
    .modal {
        width: 85%;
    }
}

.modal .close {
    position: absolute;
    top: 0;
    right: 0;
    transition: a11 200ms;
    font-size: 20px;
    font-weight: bold;
    text-decoration: none;
    color: #0a8ad8;
    padding: 5px 15px;
    background: #fff;
    box-shadow: 0 0 7px rgb(0 0 0/ 30%);
    z-index: 10;
    border-radius: 10px;
}

.modal .close:hover {
    color: #1093ea;
}

.modal .content {
    max-height: 30%;
    overflow: auto;
}

.form-container {
    background: #fff;
    font-family: 'Titillium Web', sans-serif;
    padding: 1.56rem 0.62rem;
    overflow: hidden;
    position: relative;
    z-index: 1;
}

.form-container::before {
    content: " ";
    background: radial-gradient(at 50% 25%, #1093ea 0%, #007bb7 100%);
    height: 70%;
    width: 100%;
    left: 0;
    top: 0;
    z-index: -1;
    clip-path: polygon(0 0, 100% 0%¨, 100% 100%, 0 75%);
    position: absolute;
}

.form-container .title {
    color: #fff;
    font-size: 55px;
    font-weight: 500;
    text-align: center;
    text-transform: capitalize;
    letter-spacing: 0.5px;
    margin: 0 0 1.56rem;
}

.form-container .form-horizontal {
    background: #fff;
    padding: 0.62rem;
    margin: 0 0 1.25rem;
    box-shadow: 0 0 7px rgb(0 0 0 30%);
    border-radius: 3px;
}

.form-horizontal .form-group {
    background: #fff;
    margin: 0 0 0.94rem;
    border-radius: 3px;
    border-bottom: 1px solid rgba(0, 0, 0, 0.418);
}

.form-horizontal .form-control {
    color: #555;
    background: transparent;
    font-size: 20px;
    letter-spacing: 1px;
    width: calc(100% - 50px);
    height: 2.81rem;
    padding: 0 0.31rem;
    box-shadow: none;
    border: none;
    border-radius: 0;
    display: inline-block;
    transition: all 0.3s;
}

.form-horizontal .form-group::before {
    display: table;
    content: " ";
}

.btn {
    color: #fff;
    background: #007bb0;
    font-size: 20px;
    font-weight: 600;
    text-transform: capitalize;
    letter-spacing: 1px;
    width: 100%;
    padding: 0.81rem 0.94rem 0.81rem;
    margin: 0;
    border-radius: 10px;
    transition: all 0.3s ease;
    border: none;
    cursor: pointer;
}

.user-singup {
    color: #333;
    font-size: 16px;
    font-weight: 600;
    text-align: center;
    display: block;
}
</style>