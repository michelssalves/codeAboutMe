<template>
  <div>
    <main>
        <div class="text-top">Videos novos sempre que a <strong>muié deixar gravar</strong></div>
        <a href="https://www.youtube.com/@michalves_2424" target="_blank">
            <img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg" alt="Inscreva-se" id="subscribe">
        </a>
        <div class="text-bottom">https://www.youtube.com/@michalves_2424</div>
    </main>
  </div>
</template>

<script>
export default {
    // eslint-disable-next-line
    name: 'Home',
    data(){
        return{

        }
    }
}
</script>

<style scoped>
main{
    background-color: var(--color-background-home);
    justify-content: center;
    align-items: center;
}
.text-top{
    color: var(--color-text-light);
    font-size: 16px;
      
}
#subscribe{
    width: 240px;
}
.text-bottom{

    color: var(--color-text-light);
    font-size: 18px;
    margin-top: 10px;
}
@media(min-width:700px){
    #subscribe{
        width: 470px;
    }
    .text-top{
    color: var(--color-text-light);
    font-size: 22px;
    
    }
}  
@media(max-width:350px){
    .text-top{
    color: var(--color-text-light);
    font-size: 13px;
    
    }
    .text-bottom{

    color: var(--color-text-light);
    font-size: 16px;
    margin-top: 10px;
}
} 
</style>