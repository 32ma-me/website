<script setup lang="ts">
    const props=defineProps({left:{type:String,required:true},category:String,title:String,desc:String});
</script>
<template>
    <div class="item">
        <component :is="left.split('|')[0]" :src="left.split('|')[1]" loading="lazy" :title="title" :alt="title"/>
        <div class="content">
            <p class="category">{{category}}</p>
            <p class="title">{{title}}</p>
            <p>{{desc}}</p>
        </div>
    </div>
</template>
<style scoped>
@media screen and (max-width:649px){
    iframe{
        width:calc(90vw - 1rem);
        height:calc((90vw - 1rem)/16*9);
    }
    img{
        width:calc(90vw - 1rem);
        height:calc((90vw - 1rem)/16*9);
    }
    .item{
        grid-auto-flow:row;
    }
}
@media screen and (min-width:650px){
    iframe{
        width:320px;
        height:180px;
    }
    img{
        width:320px;
        height:180px;
        align-self:center;
    }
    .item{
        grid-template-columns:320px auto;
        grid-auto-flow:column;
    }
}
iframe{
    border:none;
    align-self:center;
}
.iconify{
    margin:auto;
    width:3rem;
    height:auto;
}
.item{
    display:grid;
    grid-gap:1rem;
    max-width:calc(90vw - .5rem);
    margin-block:.5vh;
    margin-inline:.5rem;
    padding-block:1vh;
    justify-content:center;
}
.title{
    font-size:1.7rem;
    font-weight:600;
}
span{
    text-align:center;
}
.content{
    align-self:center;
    margin-block:auto;
    position:relative;
    padding-bottom:1rem;
}
p{
    margin:0;
}
.category{
    font-weight:450;
    font-size:1.2rem;
}
img{
    justify-self:center;
    object-fit:cover;
}
</style>