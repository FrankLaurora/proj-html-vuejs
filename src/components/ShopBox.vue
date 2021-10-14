<template>
    <div class="shop_box">       
        <img :src="require('../assets/img/book-widget.png')" alt="cover and kindle">
        <div class="text_box">
            <h4 class="dark">Latest Book Release</h4>
            <p class="subtitle highlighted small_text bold_text">d. vaughn autobiography</p>
            <p class="gray small_text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Facere ipsum quaerat alias. A minus recusandae alias. Numquam velit accusamus nulla dicta sapiente.</p>
        </div>
        <button class="btn btn_left dark"><i class="fab fa-amazon"></i> Buy On Amazon</button>
        <button class="btn btn_right dark"><i class="fab fa-apple"></i> Buy On AppStore</button>   
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
        
        h4 {
            line-height: 1.8rem;
        }

        img, .text_box, button {
            width: 50%;
        }
        
        button {
            padding-block: 1.1rem;
            border: 1px solid #a4d2c2;
            background-color: #f5fcfa;
            box-shadow: 0 3px 10px #a4d2c2;

            &:hover {
                background-color: #fff;
                border-color: #38d18e;
                transition: 0.1s;
            }
        }

    }
</style>