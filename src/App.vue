<script setup>
import { ref, onMounted } from 'vue';

const walk = 50;
const shadowValue = ref('');

onMounted(() => {
    window.addEventListener('mousemove', e => {
        const { clientX, clientY } = e;
        const { innerWidth: width, innerHeight: height } = window;

        console.log(clientX, clientY, width, height);

        const xWalk = Math.round((clientX / width * walk) - (walk / 2));
        const yWalk = Math.round((clientY / height * walk) - (walk / 2));

        console.log(xWalk, yWalk);

        shadowValue.value = `${xWalk}px ${yWalk}px 5px`;
    });
});

</script>

<template>
    <h1 class="title" :style="{ textShadow: shadowValue }">Text Shadow Page</h1>

    <div class="container">
        <p v-for="n in 3">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum itaque, soluta vero, necessitatibus cumque voluptates veniam commodi hic ab fuga, quia vel ea nihil sit labore nisi odio deleniti enim provident tenetur voluptas! Nisi optio distinctio animi placeat aut ex obcaecati, quia ad non laboriosam voluptate eum ipsam soluta aspernatur.</p>
    </div>
</template>

<style scoped>
    .title {
        font-size: 3rem;
        text-align: center;
        user-select: none;
    }
    .container {
        margin-top: 2rem;
        width: 100%;
        display: flex;
        gap: 2rem;
        justify-content: space-around;
        user-select: none;
    }

    .container > p {
        padding: 4rem;
    }
</style>