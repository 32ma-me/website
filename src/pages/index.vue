<template>
  <main>
    <img src="/img/avatar.webp">
    <div>
      <svg viewBox="0 0 242.6 153"><use href="/img/logo.svg#logo"/></svg>
      <h1>
        中村 栞 <wbr><span class="sub">Shio Nakamura</span>
      </h1>
      <div class="nav">
        <RouterLink to="/about"><h3>About</h3> 自己紹介</RouterLink>
        <RouterLink to="/blogs"><h3>Blogs</h3> ブログ</RouterLink>
        <RouterLink to="/skills"><h3>Skills</h3> 資格・できること</RouterLink>
        <RouterLink to="/links"><h3>Links</h3> SNS等</RouterLink>
      </div>
    </div>
  </main>
</template>

<style scoped>
@media screen and (max-width:749px){
  main{
    flex-direction:column;
    gap:20px;
    min-height:calc(100vh - 1rem - 55px);
  }
}
@media screen and (min-width:750px){
  main{
    flex-direction:row;
    gap:50px;
    min-height:calc(100vh - 55px);
  }
}
main{
  display:flex;
  justify-content:center;
  align-items:center;
  padding:0;
}
img{
  max-height:30rem;
  border-radius:5px;
}
svg{
  display:block;
  height:6rem;
}
h1{
  text-align:left;
  display:inline-flex;
  align-items:baseline;
  flex-wrap:wrap;
  gap:.25em;
  line-height:2rem;
  font-size:2.5rem;
  font-weight:300;
  margin-block:.5rem 1.5rem;
}
h1 .sub{
  font-size:1.5rem;
}
h3{
  display:inline;
  font-family:"tt-commons-pro",sans-serif;
}
.nav{
  display:flex;
  flex-direction:column;
  justify-content:center;
  flex-wrap:wrap;
  gap:.7rem;
  margin-bottom:.9rem;
}
a{
  font-weight:300;
  height:2.5rem;
  line-height:1.5em;
  display:inline-block;
  margin-right:auto;
  text-decoration:none;
  transition:none;
}
a::after{
  content:"";
  position:relative;
  bottom:.9rem;
  display:inline-block;
  height:1px;
  width:0px;
  background:rgb(var(--fg));
  transition:.2s;
}
a:hover{
    opacity:1;
}
a:hover::after{
    width:100%;
}
h3{
  display:inline;

}
</style>
