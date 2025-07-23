<script setup>

    defineProps({
        onSelect:Function
    })

</script>

<template>
     <div>
    <aside>
      <ul>
        <li><button @click="onSelect(0)">首頁</button></li>
        <li><button @click="onSelect(1)">關於我</button></li>
        <li><button @click="onSelect(2)">技能</button></li>
        <li><button @click="onSelect(3)">作品</button></li>
        <li><button @click="onSelect(4)">聯絡</button></li>
      </ul>
    </aside>

    <!-- Main Content -->
    <main>
      <slot />
    </main>
  </div>
    <footer>
        <small>Created by</small>
        <a href="https://github.com/ok037352085" target="_blank">
            <img src="https://avatars.githubusercontent.com/u/115128919?v=4" alt="pfp">
            <p>JingTung</p>
            <i class="fa-brands fa-github"></i>
        </a>
    </footer>
</template>

<style scoped>
    aside {
        position: fixed;
        top: 0;
        left: 0;
        width: 200px;
        height: 100vh;
    }

    aside ul {
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    li {
        list-style: none;
        font-size: 24px;
    }

    li button {
        border-style: none;
        outline: none;
        background: transparent;
        transition: 200ms;
        font-weight: bold;
        cursor: pointer;
    }

    li button:hover {
        transform: scale(1.2);
    }

    main {
        flex: 1;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    footer {
        width: 100%;
        display: flex;
        flex-direction: column;
        gap:  0.5rem;
        justify-content: center;
        align-items: center;
        padding: 4rem 0;
        margin-top: auto;
        position: relative;
        bottom: 0;
    }

    footer a {
        display: flex;
        align-items: center;
        gap: 0.5rem;
        padding: 0.3rem;
        padding-right: 0.5rem;
        background: #5555;
        border-radius: 4rem;
        border: 1px solid transparent;
        transition-duration: 200ms;
        text-decoration: none;
    }

    footer a:hover {
        border-color: var(--color-link);
    }

    footer a img {
        max-width: 30px;
        aspect-ratio: 1 / 1;
        border-radius: 100%;
    }
    @media (max-width: 950px) {
        aside {
            position: static;
            width: 100%;
            height: auto;
        }

        aside ul {
            flex-direction: row;
            align-items: center;
            justify-content: center;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        main {
            margin-left: 0;
            padding: 1rem;
        }
    }
</style>
