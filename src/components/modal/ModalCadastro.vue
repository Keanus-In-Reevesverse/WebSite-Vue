<template>
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
                <a href="#">Ja possui uma conta?</a>
            </label>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'ModalRegister'
})

</script>

<style lang="scss">
@import url('../../styles/css/modalBase.css');

</style>