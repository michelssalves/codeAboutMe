<template>
    <main>
        <section class="container">
            <h1>Videos</h1>
            <section class="videos">
                <div class="video" v-for="(video, index) in videosMichel" :key="index">
                    <a :href="video.link" target="_blank">
                        <img :src="video.thumb" :alt="video.title">
                        <div class="video-title">{{ video.title }}</div>
                    </a>
                </div>
            </section>
         
        </section>
    </main>
</template>

<script>
export default {
    // eslint-disable-next-line
    name: 'Videos',
    data() {
        return {
            videos: [],
            videosMichel: [
                { title: 'Driver 2', link: 'https://www.youtube.com/watch?v=Z8_HsT6q1c0&ab_channel=NubSaiBot', thumb:'https://muralgamer.com/wp-content/uploads/2013/10/driver-2-1.jpg'},
                { title: 'Warzone 2', link: 'https://youtu.be/nAXuNZsPVqw?si=W6ar5G9gZJ03BGClt', thumb:'https://t2.tudocdn.net/645585?w=1920'},
                { title: 'Horizon Zero Dawn', link: 'https://www.youtube.com/watch?v=tnlO0FKHSsA&ab_channel=NubSaiBot', thumb:'https://cdn-ext.fanatical.com/production/product/1280x720/d5f7dc78-2c2d-4604-90ee-79ca108c01fc.jpeg'},
            ]
        }
    },
    mounted() {
        this.$http.get('/videos.json').then(res => {
            console.log(res)
            this.videos = res.data

        })
    },
}
</script>

<style>
main {
    align-items: center;
}

.videos {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.video {
    widows: 80%;
    margin-bottom: 30px;
}

.video img {
    width: 100%;
}

.video a {
    color: var(--color-text-dark);
    font-weight: 600;
    text-align: center;

}

@media (min-width:700px) {
    .videos {
        flex-direction: row;
        align-items: flex-start;
        flex-wrap: wrap;
    }

    .video {

        margin-right: 30px;
        width: 300px;
    }

}
</style>