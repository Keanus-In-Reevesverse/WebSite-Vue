<template>
    <div class="footer">
        <p>&copy; 2022</p>
    </div>
</template>


<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'SkirtingFooter'
})
</script>

<style lang="scss" scoped>
.footer{
    display:flex;
    justify-content:center;
    color: black;
    background-color: rgb(87, 86, 86);
    padding: 5rem;
    width: 100%;

    p{
        font-family: var(--cartoon-font);
        font-weight:700;
        font-size: 20px;
    }
}
</style>
