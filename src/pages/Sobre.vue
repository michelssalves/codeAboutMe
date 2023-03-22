<template>
    <main>
        <section class="container">
            <h1>Sobre</h1>
            <div class="about" v-html="aboutMichel">
               
            </div>
        </section>
    </main>
</template>

<script>
export default {
    // eslint-disable-next-line
    name: 'Sobre',
    data() {
        return {
            about: '',
            aboutMichel:"Trabalhei na Estre Ambiental de MAR/2011 a ABR/2022, iniciei como aprendiz,<br><br> Fui efetivado para Auxiliar Administrativo, Comprador, Analista de Dados e Analista de Suporte de T.I, <br><br>Nessa área eu finalmente me encontrei profissionalmente e meu olhos foram abertos para minha verdadeira vocação que é usar a tecnologia para melhorar e facilitar a vida das pessoas a minha volta.<br><br>Nesse periodo tive grande envolvimento com o sistema SAP nos modulos PM e MM e desenvolvi o sistema Controle de Abastecimento que informatizou a forma de controle do consumo de Diesel da empresa.<br><br>Estou trabalhando na RDP-Petroleo desde ABR/2022 como Programador PHP e em paralelo participando da implantação do Sistema Totvs.<br><br>Sou formado em Analise e Desenvolvimento de Sistemas<br><br>Meus conhecimentos de programação são CSS, JavaScript, VueJS, PHP, Laravel, Mysql, Sybase, GitHub, Postman, Axios, Rest."
        }
    },
    mounted() {
        this.$http.get('/about.json').then(res => {

            this.about = res.data.about

        })
    },
}
</script>

<style>
main {
    align-items: center;
}
.about{
    margin-bottom: 40px;
    color:var(--color-text-dark);
}

</style>