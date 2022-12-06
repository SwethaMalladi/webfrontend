<template>
     <div class="Network_Box">
        <div v-for="networks in networks" :key="networks.id" >         
                <Network_Item :networks="networks"/>
         </div>
     <!--<img url = "https://www.att.com/idpassets/global/devices/phones/apple/apple-iphone-14-pro/carousel/deeppurple/deeppurple1.png"> -->
     </div>
      
</template>

<script>

import Network_Item from "./Network_Item.vue"
export default{
    name: 'Network_Box',
    components: {
        Network_Item
    },
    props: {
        networks: Array
    }
}
</script>

<style>

.Network_Box{

    width : 90%;
    height: 90%;
    background-color: rgb(13, 12, 16);
    padding: 1em;
    color: rgb(233, 160, 223);
    display: grid;
    /*grid-template-columns: repeat(2, minmax(300px, 1.5fr));
    grid-template-rows: repeat(5, 1fr);*/
    grid-template-columns: 1fr;
    grid-gap: 20px;
    align-items: stretch;
    font-size: 2vmin;
    margin: 5% 5% 5% 5%;
    /*background-image: url("https://t3.ftcdn.net/jpg/04/49/47/16/360_F_449471656_6tH7Glz5CtouQAPNM9188r4ozu0hlv0t.jpg");
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-size: cover;*/
    background-image: url("https://www.att.com/idpassets/global/devices/phones/apple/apple-iphone-14-pro/carousel/deeppurple/deeppurple1.png");
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-size: 40% ;
    background-position: right;
}
</style>