<template>
    <div class="about md_container">
        <h2>More About Damon Vaughn</h2>
        <p>Damon Vaughn is a professor of psychology at the University of Toronto, a clinical psychologist and the author of the multi-million copy bestseller "The story of my life."</p>
        <button class="btn btn_green">Meet the Author</button>
    </div>
</template>

<script>
export default {
    name: 'About'
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