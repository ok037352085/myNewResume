<script setup>
       defineProps({
        onSelect:Function
    })

</script>

<template>
    <div class="container">
        <img src="https://avatars.githubusercontent.com/u/115128919?v=4" alt="pfp">
        <p>我叫葉勁桐，我是自學成長的前端工程師，大學主修遊戲程式設計。 <br/>一步步從遊戲程式轉職到前端程式設計，熱愛把想法變成有溫度的網站。</p>
        <div class="link">
            <li><button @click="onSelect(1)">關於我 &rarr;</button></li>
            <li><button @click="onSelect(3)">作品集 &rarr;</button></li>
        </div>
    </div>
</template>

<style scoped>
    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 3rem;
        width: 700px;
        height: 75vh;
    }

    .container img {
        width: 100%;
        max-width: 400px;
        aspect-ratio: 1 / 1;
        border-radius: 50%;

    }

    .container .link li {
        list-style: none;
    }

    .link {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .link button {
        background: transparent;
        outline: none;
        border-style: none;
        transition: 200ms;
    }

    .link button:hover {
        transform: scale(1.2);
    }

    @media (max-width: 640px) {
        .container {
        max-width: 500px;
        }

        .container img{
            max-width: 300px;
        }
    }
</style>
