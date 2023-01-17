<script setup>

</script>

<template>
    <h1 class="title">Text Shadow Page</h1>

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