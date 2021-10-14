<template>
    <section class="about md_container" id="about">
        <h2 class="highlighted">{{about.title}}</h2>
        <p class="big_text">{{about.content}}</p>
        <button class="btn btn_green">Meet the Author</button>
    </section>
</template>

<script>
export default {
    name: 'About',
    
    props: {
        about: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';
    
    .about {
        text-align: center;
        padding-block: 128px;
        padding-inline: 80px;
        
        p {
            line-height: 3rem;
            margin-bottom: 55px;
        }
    }


</style>