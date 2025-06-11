<script setup>

</script>

<template>
  <section class="about-me">
    <h1 class="title">關於我</h1>
    <p class="intro">
      我是一位剛畢業的大學生，專注於前端開發，熱愛使用 Vue 打造簡潔、高效的使用者介面。
      喜歡挑戰新技術，對於寫出清晰可維護的程式碼充滿熱情。
    </p>

    <div class="details">
      <p><strong>姓名：</strong> 葉勁桐</p>
      <p><strong>學歷：</strong> 私立育達科技大學 多媒體與遊戲設計系</p>
      <p><strong>專長：</strong> Vue 3、HTML、CSS、JavaScript、Git</p>
      <p><strong>目標：</strong> 成為一名能夠獨立開發前端專案的工程師</p>
    </div>
  </section>
</template>

<style scoped>
  .about-me {
    max-width: 700px;
    margin: 80px auto;
    padding: 0 20px;
    font-family: sans-serif;
    line-height: 1.8;
  }

  .title {
    font-size: 28px;
    font-weight: bold;
    margin-bottom: 20px;
    border-left: 4px solid #333;
    padding-left: 12px;
   }

  .intro {
    margin-bottom: 24px;
    font-size: 18px;
  }

  .details p {
    margin: 8px 0;
    font-size: 16px;
  }
  /* 手機版調整 */
@media (max-width: 640px) {
  .about-me {
    margin: 40px auto;
    padding: 0 16px;
  }

  .title {
    font-size: 2rem;
  }

  .intro {
    font-size: 1rem;
  }

  .details p {
    font-size: 0.95rem;
  }
}
</style>
