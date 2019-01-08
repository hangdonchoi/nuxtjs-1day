<template>
  <div class="single-post-page">
    <section class="post">
      <h1 class="post-title">포스트타이틀</h1>
      <div class="post-details">
        <div class="post-details"> 업데이트 일자</div>
        <div class="post-details"> 작성자</div>
      </div>
      <p> 포스트 내용</p>
    </section>
    <section class="post-feedback">
      <p>안녕하세요 하하하하 반갑습니다.</p>
    </section>
  </div>
</template>

<script>
export default {}
</script>

<style>
.single-post-page {
  padding: 30px;
  text-align: center;
  box-sizing: border-box;
}

.post {
  width: 100%;
}

@media (min-width: 768px) {
  .post {
    width: 600px;
    margin: auto;
  }
}

.post-title {
  margin: 0;
}

.post-details {
  padding: 10px;
  box-sizing: border-box;
  border-bottom: 3px solid #ccc;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

@media (min-width: 768px) {
  .post-details {
    flex-direction: row;
  }
}

.post-detail {
  color: rgb(88, 88, 88);
  margin: 0 10px;
}

.post-feedback a {
  color: red;
  text-decoration: none;
}

.post-feedback a:hover,
.post-feedback a:active {
  color: salmon;
}
</style>
