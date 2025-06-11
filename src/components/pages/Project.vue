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
    tech: 'Vue, Vite, Node.js, LocalStorage',
    demo: 'https://ok037352085.github.io/TodoList/',
    code: 'https://github.com/your-todo-app',
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
</style>
