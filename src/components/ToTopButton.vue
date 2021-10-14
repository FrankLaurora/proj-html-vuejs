<template>
    <a href="#home">
        <div class="button_to_top">
            <i class="fas fa-chevron-up"></i>
        </div>
    </a>
</template>

<script>
export default {
    name: 'ToTopButton'
}
</script>

<style lang="scss" scoped>
.button_to_top {
    position: fixed;
    bottom: 50px;
    right: 100px;
    display: block;
    height: 2.5rem;
    width: 2.5rem;
    text-align: center;
    line-height: 2.5rem;
    color: #fff;
    background-color: rgba(0, 0, 0, 0.5);
    border-radius: 0.5rem;

    &:hover {
      transform: scale(1.1);
    }
  }
</style>