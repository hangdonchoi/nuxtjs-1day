<template>
  <div class="home-page">
    <section class="intro">
      <h1> 블로그 리스트</h1>

    </section>
    <section class="featured-posts">
      <!-- <nuxt-link 
        :to="'/posts/'+1" 
        class="post-preview">
        <article >
          <div 
            class="post-thumbnail" 
            style="background-image:url('https://images.readwrite.com/wp-content/uploads/2018/04/coding-825x500.jpg')">썸네일1</div>
          <div class="post-content">
            <h1>포스트제목</h1>
            <h1>프리뷰글</h1>
          </div>
        </article>
      </nuxt-link> -->
      <!-- <PostPreview/>
      <PostPreview/>
      <PostPreview/> -->
      <!--3차로 해보자-->
      <PostPreview 
        id="1" 
        thumbnail="https://images.readwrite.com/wp-content/uploads/2018/04/coding-825x500.jpg" 
        title="제목입니다."
        preview-text="내용입니다긂"/>
    </section>
  
  </div>
</template>

<script>
//여기서부터는 Posts components  개발하고 나서 생성하게 됨
import PostPreview from '@/components/Posts/PostPreview'
export default {
  components: {
    PostPreview
  }
}
//여기서부터는 Posts 개발하고 나서 생성하게 됨
</script>

<style scoped>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url('~assets/images/main-page-background.jpg');
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}

.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}

.post-preview {
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #ccc;
  background-color: white;
  width: 90%;
}

a {
  text-decoration: none;
  color: black;
}

@media (min-width: 850px) {
  .post-preview {
    width: 400px;
    margin: 10px;
  }
}

.post-thumbnail {
  width: 100%;
  height: 200px;
  background-position: center;
  background-size: cover;
}

.post-content {
  padding: 10px;
  text-align: center;
}

a:hover .post-content,
a:active .post-content {
  background-color: #ccc;
}
</style>
