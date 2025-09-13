<script setup>
    const projects = [
  {
    title: '紀錄帳號的小網頁',
    description: '使用Html + CSS + JavaScript 製作。  簡單但實用，讓我不需要一直點擊 "忘記密碼"。',
    tech: 'Html, CSS, JavaScript, LocalStorage',
    demo: 'https://ok037352085.github.io/myAccounts/',
    code: 'https://github.com/ok037352085/myAccounts',
  },
  {
    title: 'Todo 應用程式',
    description: '除了基本的todolist，還新增了日歷的功能，在日曆上選擇要添加待辦事項的日期，並在該日期新增/刪除待辦事項。',
    tech: 'Vue3, Vite, Node.js, LocalStorage',
    demo: 'https://ok037352085.github.io/TodoList/',
    code: 'https://github.com/ok037352085/TodoList',
  },
  {
    title: '天氣查詢應用程式',
    description: '輸入城市名稱，即可查詢天氣資訊。使用 Vue 3 組件化架構，具備錯誤處理與 Loading 動畫，並支援 RWD。',
    tech: 'Vue3, Vite, OpenWeatherMap API,',
    demo: 'https://ok037352085.github.io/WeatherAPI/',
    code: 'https://github.com/ok037352085/WeatherAPI',
  },
  {
    title:'苗栗地方旅遊網站',
    description: '苗栗地方旅遊網，註冊會員即可自選景點組成一個行程保存，還能留言，並在網站上顯示',
    tech: 'vue3, Vite, Firebase, LocalStorage, ',
    demo: 'https://ok037352085.github.io/PHPTravelWebSite/',
    code: 'https://github.com/ok037352085/PHPTravelWebSite/'
  },
  {
    title:'Spotify音樂搜尋器',
    description:'利用SpotifyAPI 實現登入、音樂查詢並撥放(需要premium)',
    tech:'Vue3, Vite, LocalStorage, SpotifyAPI',
    demo:'https://ok037352085.github.io/SpotifyAPI/',
    code:'https://github.com/ok037352085/SpotifyAPI'
  }
]
</script>

<template>
     <section class="projects">
    <h1>作品集</h1>

    <div class="project-list">
      <div v-for="(project, index) in projects" :key="index" class="project-card">
        <h2>{{ project.title }}</h2>
        <p>{{ project.description }}</p>
        <p><strong>技術：</strong> {{ project.tech }}</p>
        <div class="links">
          <a :href="project.demo" target="_blank" v-if="project.demo">Live Demo &rarr;</a>
          <a :href="project.code" target="_blank" v-if="project.code">GitHub  <i class="fa-brands fa-github-alt"></i></a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
    .projects {
        max-width: 800px;
        margin: 80px auto;
        font-family: sans-serif;
        padding: 0 20px;
    }

    .projects h1 {
        font-size: 28px;
        margin-bottom: 24px;
        border-left: 4px solid #333;
        padding-left: 12px;
    }

    .project-list {
        display: grid;
        gap: 24px;
    }

    .project-card {
        border: 1px solid #ddd;
        padding: 20px;
        border-radius: 12px;
        transition: 0.2s;
    }

    .project-card:hover {
        box-shadow: 0 4px 12px rgba(0,0,0,0.5);
    }

    .project-card h2 {
        margin-bottom: 8px;
    }

    .links {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .links a {
        margin-right: 12px;
        color: #007acc;
        text-decoration: none;
        font-size: 14px;
        transition: 200ms;
    }

    .links a:hover {
        transform: scale(1.2);
    }

    @media (max-width: 940px) {
      .project-card {
        margin: 0 100px;
      }
    }
</style>
