<template>
    <Window :window="this.meta">
        <template slot="content">
                <aplayer autoplay :music="this.firstMusic"
                         :list="this.musicList"
                         repeat="repeat-all"
                         theme="#2A2B2B" class="w-full h-full" style="margin: 0"
                />
        </template>
    </Window>
</template>

<script>
    import Window from "../window/Window";
    import Aplayer from 'vue-aplayer'

    export default {
        name: "Music",
        components: {Window, Aplayer},
        props: {
            meta: {
                type: Object,
                required: true,
            }
        },
        mounted() {
        },
        data() {
            return {
                musicList: [
                    {
                        "title":"だから僕は音楽を辞めた (所以我放弃了音乐)",
                        "artist":"ヨルシカ (Yorushika)",
                        "src":"https://oss.wendemoapi.site/ta-01/5daad1f8-de0d-e303-f036-d344a14fab81.mp3",
                        "pic":"/music/m0.png"
                    },
                    {
                        "title":"Песня о тревожной молодости",
                        "artist":"Хор Московского Сретенского монасты",
                        "src":"https://oss.wendemoapi.site/ta-01/b27523db-4b9b-bbed-ec12-a8b8afc8fd85.mp3",
                        "pic":"/music/m1.png"
                    },
                    {
                        "title":"あの微笑みを忘れないで",
                        "artist":"ZARD (ザード)",
                        "src":"https://oss.wendemoapi.site/ta-01/df1c22f6-6ba8-0a97-f4ac-6aef7f4fbc57.mp3",
                        "pic":"/music/m2.png"
                    },
                    {
                        "title":"告白の夜 (告白之夜) (LIVE!! Ayasa Theater episode 7)",
                        "artist":"Ayasa绚沙",
                        "src":"https://oss.wendemoapi.site/ta-01/f1be7233-eec6-012f-a0e1-e6edf97dccc3.mp3",
                        "pic":"/music/m3.png"
                    },
                    {
                        "title":"红楼梦序曲",
                        "artist":"陈力",
                        "src":"https://oss.wendemoapi.site/ta-01/56e4f8cd-7973-1930-d2cc-c3957afa414e.mp3",
                        "pic":"/music/m4.png"
                    },
                    {
                        "title":"I'll remember you",
                        "artist":"佐坂めぐみ",
                        "src":"https://oss.wendemoapi.site/ta-01/1491e002-f300-6c05-28ba-d321c47a86f8.mp3",
                        "pic":"/music/m5.png"
                    },
                    {
                        "title":"永遠の嘘をついてくれ (给我一个永远的谎言)",
                        "artist":"中島みゆき",
                        "src":"https://oss.wendemoapi.site/ta-01/85403895-bc58-7918-dc75-5f0d4ddd14da.mp3",
                        "pic":"/music/m6.png"
                    },
                    {
                        "title":"象",
                        "artist":"高橋 優 (たかはし ゆう)",
                        "src":"https://oss.wendemoapi.site/ta-01/57754788-cea5-74f8-d7bc-98418c75dbb0.mp3",
                        "pic":"/music/m7.png"
                    },
                    {
                        "title":"月牙湾",
                        "artist":"F.I.R.飞儿乐团",
                        "src":"https://oss.wendemoapi.site/ta-01/0fdc2b9a-15be-7801-87ef-75730fc92f9e.mp3",
                        "pic":"/music/m8.png"
                    },
                    {
                        "title":"Cry Cry",
                        "artist":"T-ara (티아라)",
                        "src":"https://oss.wendemoapi.site/ta-01/e21b27a7-3518-9cbb-d4aa-f96b12a43b24.mp3",
                        "pic":"/music/m9.png"
                    },
                    {
                        "title":"Twinkle Starlight",
                        "artist":"佐咲 紗花 (ささき さやか)",
                        "src":"https://oss.wendemoapi.site/ta-01/1eb92111-1962-1666-a6f8-ca81cb51cb67.mp3",
                        "pic":"/music/m10.png"
                    },
                    {
                        "title":"Komm, süsser Tod (甘き死よ、来たれ)",
                        "artist":"ARIANNE",
                        "src":"https://oss.wendemoapi.site/ta-01/5b71dd18-505d-07bc-bebf-57e7a0be2d62.mp3",
                        "pic":"/music/m11.png"
                    },
                    {
                        "title":"在太行山上",
                        "artist":"中国交响乐团合唱团",
                        "src":"https://oss.wendemoapi.site/ta-01/d6ab4aac-b458-8413-f3e4-4a8cc4062682.m4a",
                        "pic":"/music/m12.png"
                    },
                    {
                        "title":"エンジェルウインク (Angel Wink)",
                        "artist":"茅野愛衣 (かやの あい)",
                        "src":"https://oss.wendemoapi.site/ta-01/48a3a925-4753-e602-fa50-1bfbfc9d0895.mp3",
                        "pic":"/music/m13.png"
                    },
                    {
                        "title":"La Reine De Saba",
                        "artist":"Paul Mauriat",
                        "src":"https://oss.wendemoapi.site/ta-01/12da445c-7cf5-8d06-e78e-0deededf090f.mp3",
                        "pic":"/music/m14.png"
                    },
                    {
                        "title":"シルエット・ダンサー",
                        "artist":"今井優子 (いまい ゆうこ)",
                        "src":"https://oss.wendemoapi.site/ta-01/2d362db6-e6c0-c6ee-866a-74d4f5c69856.mp3",
                        "pic":"/music/m15.png"
                    },
                    {
                        "title":"and I'm home",
                        "artist":"喜多村英梨 (きたむら えり)",
                        "src":"https://oss.wendemoapi.site/ta-01/597a457f-0a2d-8002-d32e-d20080d9accd.mp3",
                        "pic":"/music/m16.png"
                    }
                ],
                firstMusic: {
                    "title":"だから僕は音楽を辞めた (所以我放弃了音乐)",
                    "artist":"ヨルシカ (Yorushika)",
                    "src":"https://oss.wendemoapi.site/ta-01/5daad1f8-de0d-e303-f036-d344a14fab81.mp3",
                    "pic":"/music/m0.png"
                },
            }
        },
        methods: {
        }
    }
</script>
