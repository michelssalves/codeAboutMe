<template>
    <footer>
        <a class="socialLink" v-for="(socialLink, index) in socialLinksMichel" :key="index" :href="socialLink.link" target="_blank">
            <img :alt="socialLink.label" :src="socialLink.icon" :title="socialLink.label">
        </a>
    </footer>
</template>

<script>
export default {
    // eslint-disable-next-line
    name: 'Footer',
    data(){
        return{
            socialLinks:[],
            socialLinksMichel:[   
            { icon: 'https://imagepng.org/wp-content/uploads/2017/08/instagram-icone-icon-1.png', link: 'https://www.instagram.com/michelssalves/', label:'Instagram'},
            { icon: 'https://cdn-icons-png.flaticon.com/512/1384/1384060.png', link: 'https://www.youtube.com/channel/UCKhDgQw2A3Gif4N5-2Qy1Bg', label:'Youtube'},
            { icon: 'https://logospng.org/download/linkedin/logo-linkedin-icon-2048.png', link: 'https://www.linkedin.com/in/michel-alves-05a41813b/', label:'LinkedIn'},
            { icon: 'https://freepngimg.com/thumb/whatsapp/77220-scalable-vector-graphics-logo-whatsapp-icon.png', link: 'https://web.whatsapp.com/send/?phone=5541984382660&text=Ol%C3%A1%2C+como+voc%C3%AA+est%C3%A1%3F&type=phone_number&app_absent=0', label:'WhatsApp'},    
            ],
        }
    },
    mounted() {
        this.$http.get('/social-links.json').then(res => {

            console.log(res)
            this.socialLinks = res.data

        }) 
    },
}
</script>

<style scoped>
    footer{
        width: 100%;
        height: 60px;
        background-color: var(--color-background-nav);
        display: flex;
        justify-content: center;
        justify-items: center;
    }
    .socialLink{
        /*border:2px solid var(--color-text-light);*/
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 50%;
        width: 40px;
        height: 40px;
        margin: 0 10px;
        margin-top: 10px ;
    }
    .socialLink img{
        
        width: 25px;
        border-radius: 5px;

    }
</style>

