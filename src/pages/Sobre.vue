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
            aboutMichel:` 
            <div style="text-align: justify;">               
                <p> Olá! Sou um profissional dedicado e apaixonado por tecnologia, com experiência e crescimento ao longo de uma jornada enriquecedora. Iniciei minha carreira na Estre Ambiental em março de 2011 como aprendiz e, ao longo dos anos, tive a oportunidade de desempenhar diferentes papéis, evoluindo para posições de destaque, como Analista de Dados e Analista de Suporte de T.I. Essa trajetória me proporcionou o encontro com minha verdadeira vocação: utilizar a tecnologia para melhorar e facilitar a vida das pessoas ao meu redor.</p><br>

                <p>Durante minha atuação na Estre Ambiental, tive a oportunidade de me aprofundar em sistemas, principalmente o <strong>SAP</strong>, nos módulos <strong>PM</strong> e <strong>MM</strong>. Além disso, desenvolvi um sistema de Controle de Abastecimento, que informatizou e otimizou o controle do consumo de Diesel na empresa.</p>

                <p>Atuei na RDP-Petróleo de abril de 2022 a fevereiro de 2024, como <strong>Programador PHP</strong>, participando ativamente da <strong>implantação do Sistema Totvs</strong>. Nessa nova fase da minha carreira, venho ampliando meu conhecimento nos módulos de <strong>Compras, Faturamento, Financeiro, APSDU e Configurador</strong>, o que me permite contribuir de forma abrangente para essa área de atuação.</p><br>

                <p>Atuei como <strong>Analista de Suporte ERP TOTVS na Construtora Elevação</strong>, atuando diretamente com suporte ao usuário nas atividades de <strong>emissão de nota de saída, importação via XML, importação via Mile</strong>, entre outros.</p><br>

                <p>Atualmente estou como <strong>Programador ADVPL</strong> na Terminal de Contêineres de Paranaguá, onde minhas principais atividades têm sido criar <strong>integrações Protheus com uma API de terceiros, criar relatórios e realizar manutenção em bugs apresentados pelo sistema</strong>.</p><br>

                <p>Sou formado em Análise e Desenvolvimento de Sistemas, o que me proporcionou uma sólida base técnica. Meus conhecimentos em programação incluem <strong>ADVPL, POUI Angular, VueJS, Laravel, MySQL, Sybase, SQL Server, GitHub, Postman e API Rest</strong>, o que me permite trabalhar com eficiência e qualidade nas mais diversas tarefas.</p><br>

                <p>Estou sempre em busca de novos desafios e aprendizados, buscando me aprimorar constantemente para acompanhar o dinamismo do mundo da tecnologia. Se você procura um profissional comprometido, criativo e apaixonado por tecnologia, não hesite em entrar em contato comigo.</p><br>

                <p>Convido você a explorar meu perfil no GitHub: <a href="https://github.com/michelssalves">https://github.com/michelssalves</a>, onde compartilho alguns dos meus projetos e trabalhos.</p>

                <p>Caso queira entrar em contato, fique à vontade para me ligar ou me chamar no WhatsApp: <strong>(41) 98438-2660</strong>. Estou aberto a oportunidades de crescimento e colaboração, prontamente disponível para contribuir com meu conhecimento e habilidades em projetos desafiadores.</p>
            </div>
                `
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