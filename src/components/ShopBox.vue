<template>
    <div class="shop_box">       
        <img :src="require('../assets/img/book-widget.png')" alt="cover and kindle">
        <div class="text_box">
            <h4>Latest Book Release</h4>
            <h5 class="small_text">d. vaughn autobiography</h5>
            <p class="small_text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Facere ipsum quaerat alias. A minus recusandae alias. Numquam velit accusamus nulla dicta sapiente.</p>
        </div>
        <button class="btn_left small_text"><i class="fab fa-amazon"></i> Buy On Amazon</button>
        <button class="btn_right small_text"><i class="fab fa-apple"></i> Buy On AppStore</button>   
    </div>
</template>

<script>
export default {
    name: 'ShopBox'

}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';
    
    .shop_box {
        position: absolute;
        bottom: 0;
        right: 0;
        display: flex;
        flex-wrap: wrap;
        width: 36%;
        background-color: #ffffff;
        padding: 50px 70px 40px;

        h5, button {
            font-family: 'Roboto', sans-serif;
        }
        
        h4, h5 {
            line-height: 1.8rem;
        }

        h5 {
            text-transform: uppercase;
            color: $highlighted-text;
        }

        p {
            line-height: 1.5rem;
        }

        img, .text_box, button {
            width: 50%;
        }
        
        button {
            padding-block: 1.1rem;
            border: 1px solid rgba($btn-primary, 0.5);
            background-color: rgba($btn-primary, 0.1);
            box-shadow: 0 3px 10px $btn-primary;
            font-weight: 500;

            &:hover {
                background-color: #fff;
                border-color: $btn-primary;
            }
        }

    }
</style>