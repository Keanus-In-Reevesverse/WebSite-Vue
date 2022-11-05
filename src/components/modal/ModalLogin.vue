<template>
    <div id="modalLogin" class="modalOverlay">
        <div class="modal">
            <a href="#" class="close">&times;</a>
            <div class="content">
                <div class="form-container">
                    <h3 class="title">Login</h3>
                    <form action="" class="form-horizontal">
                        <div class="form-group">
                            <input type="email" class="form-control" placeholder="Insira o email">
                        </div>

                        <div class="form-group">
                            <input type="password" class="form-control" placeholder="Insira a senha">
                        </div>

                        <label class="forget">
                            <a href="modalforget.html">Esqueceu a senha?</a>
                        </label>
                        <button class="btn">Login</button>
                    </form>

                    <label class="user-singup">
                        <a href="modalcasdastro.html">Ainda não tem uma conta?</a>
                    </label>
                </div>
            </div>
        </div>
    </div>
</template>


<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'ModalLogin'
})
</script>

<style lang="scss">
@import url('../../styles/css/modalBase.css');

</style>