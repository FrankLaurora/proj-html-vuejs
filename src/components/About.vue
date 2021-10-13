<template>
    <section class="about md_container">
        <h2>{{about.title}}</h2>
        <p>{{about.content}}</p>
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

        h2 {
            color: $highlighted-text;
        }
        
        p {
            font-family: 'Roboto', sans-serif;
            font-size: 1.5rem;
            line-height: 3rem;
            margin-bottom: 55px;
        }
    }


</style>