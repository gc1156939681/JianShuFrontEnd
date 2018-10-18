<template xmlns="http://www.w3.org/1999/html">
  <div>
    <b-col  cols="9">
      <div class="row top">
        <b-col  cols="2">
          <img class="avatar" src="//upload.jianshu.io/collections/images/4/sy_20091020135145113016.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/240/h/240">
        </b-col>
        <b-col  cols="4" class="topic-name-location">
          <span class="topic-name">读书</span>
          <p class="article-count" >收录了182940篇文章 · 3508185人关注</p>
        </b-col>

        <div class="btn-location">
          <b-button  variant="outline-success" size="mg" class="contribute">投稿</b-button>
          <div class="login-btn-location"><input type="button" class="login-btn btn btn-block" value="+关注"></div>
        </div>
      </div>


      <div>
        <div class="row out-set" v-for="article in topic.articleList" :key="article.id" >
          <b-col  cols="8">
            <p style="font-size: 18px;font-weight: bold;color: #333;padding-top: 6%">{{article.title}}</p>
            <p style="color: grey;font-size: 12px;color: gray;letter-spacing: 1px">{{article.introduction}}</p>
            <div class="line">
              <img  :src="article.icon1" class="icon1">
              <p class="amount-text">{{article.amount1}}</p>
              <img  :src="article.icon2" class="icon2">
              <p class="amount-text">{{article.amount2}}</p>
              <img  :src="article.icon3" class="icon3">
              <p class="amount-text">{{article.amount3}}</p>
              <p class="amount-text time-location">{{article.time}}</p>
            </div>


          </b-col>
          <b-col  cols="4" style="margin-top:5%">
            <img :src="article.url" class="picture">
          </b-col>
        </div>

      </div>

    </b-col>

    <b-col cols="3">

    </b-col>
  </div>

















    <!--<h4>专题{{id}}详情</h4>-->
    <!--<b-row>-->
      <!--<b-col cols="8">-->
        <!--<b-media vertical-align="center" class="article-box">-->
          <!--<img :src="topic.topicUrl" class="article-thumbnail"/>-->
          <!--<h6 class="mt-0 mb-1 title">{{topic.topicName}}</h6>-->
          <!--<p class="abstract">-->
            <!--<span>收藏了{{topic.articleCount}}篇文章,{{topic.fans}}关注</span>-->
          <!--</p>-->
        <!--</b-media>-->
      <!--</b-col>-->
    <!--</b-row>-->



</template>

<script>
  import vArticle from '../page/Article';
  export default {
    components:{
      vArticle
    },
    data() {
      return {
        id: this.$route.params.id,
        topic: {},
        articleList: [],
        fansList:[]
      }
    },
    activated() {
      this.id = this.$route.params.id;
      console.log(this.id);
      if (this.id == 1) {
        var t = {
          "id": 1,
          "topicName": "读书",
          "topicUrl": "//upload.jianshu.io/collections/images/4/sy_20091020135145113016.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/240/h/240",
          "summary": "读书读书读书读书读书读书读书读书",
          "articleCount": 49535,
          "fans": 1601,
          "description":"fdfdf",
          "creator":"简书",
          "articleList":[
            {
              "id":1,
              "title":"今天种下一颗种子，来日望成参天大树",
              "summary":"女儿放学回家，见我在看书，凑过来问道：“妈妈，你看什么呀？” 我眼睛没离开书本：“在看一种植物，它居然还能吃肉。” “真的吗？有这种植物？那给我...",
              "thumbnail":"https://upload-images.jianshu.io/upload_images/13324384-da22400366610f18.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
              "authorId":1,
              "nickName":"钱多多在简书",
              "comments":1,
              "likes":3
            },
            {
              "id":2,
              "title":"《聚是一团火，散是满天星》：远去的1977年",
              "summary":"001作者是谁？ 《聚是一团火，散是满天星》是作者王熙远编写的一本散文集，身为主编人，不得不提到王熙远与此书的缘分。 王熙远出生于上世纪50年代...",
              "thumbnail":"https://upload-images.jianshu.io/upload_images/1513087-43040419fa1fe84a.png?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
              "authorId":2,
              "nickName":"桑笛说",
              "comments":104,
              "likes":42
            },
            {
              "id":3,
              "title":"读书丨哲学家们都干了些什么：哲学，哲学家与我们的生活",
              "summary":"哲学是一门看上去“无用”的学科，讨论各种“为什么”，比如：世界的本质是什么？什么知识是真实的？人生活的意义又是什么？听起来离我们的日常生活似乎很...",
              "thumbnail":"https://upload-images.jianshu.io/upload_images/11267658-aa7f21fddce881a5.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
              "authorId":3,
              "nickName":"桑笛说",
              "comments":104,
              "likes":42
            },
            {
              "id":4,
              "title":"读书丨哲学家们都干了些什么：哲学，哲学家与我们的生活",
              "summary":"哲学是一门看上去“无用”的学科，讨论各种“为什么”，比如：世界的本质是什么？什么知识是真实的？人生活的意义又是什么？听起来离我们的日常生活似乎很...",
              "thumbnail":"https://upload-images.jianshu.io/upload_images/11267658-aa7f21fddce881a5.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
              "authorId":4,
              "nickName":"慕灵珊",
              "comments":2,
              "likes":14
            },
            {
              "id":5,
              "title":"笛安丨一个我喜欢的女子",
              "summary":"芙蓉如面柳如眉，对此如何不泪垂？ 今天突然推荐作者是因为我刷微博的时候突然知道了龙城三部曲的影视版权早就被天娱买了下来，有一丝难过。 .",
              "thumbnail":"https://upload-images.jianshu.io/upload_images/11408038-a5420dbd9afd1909.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
              "authorId":5,
              "nickName":"不认识先生的蟹蟹小姐",
              "comments":4,
              "likes":124
            },
            {
              "id":6,
              "title":"【读书】有我之境与无我之境",
              "summary":"文/月照琴台 女儿高考时，我给她买了很多练习题，其中有套诗词鉴赏练习，我因为喜欢也没舍得扔，时常偷空拿来练习，权当自我提高。 今天随手翻阅碰到一...",
              "thumbnail":"https://upload-images.jianshu.io/upload_images/11025104-75877706f921fac9.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
              "authorId":6,
              "nickName":"慕灵珊",
              "comments":12,
              "likes":43
            },


          ],
          "fansList":[
            {
              "authorId":3,
              "avatar":"11.png"
            }
          ]
        };
        this.topic = t;
      } else {
        this.topic = {};
      }
    },
    computed: function () {
      return this.topic;
    }
  }
</script>

<style scoped>
  .top{
    padding-top:3%;
    padding-bottom: 4%;
    margin-left: 8%;
    display: flex;
  }
  .avatar{
    width: 76px;
    height:76px;
    border-radius: 6%;
  }
  .topic-name{
    font-size: 20px;
    font-weight: bold;
    color: #333;
  }
  .topic-name-location{
    /*margin-left: 1%;*/
    margin-top: 4px;
  }
  .article-count{
    font-size: 13px;
    color: gray;
    margin-top:2%;
  }
  .button-location{
    /*margin-top: 2%;*/
    display: flex;
    margin-left:6px;

  }
  .login-btn{
    background-color: #42c02e;
    border-radius: 30px;
    font-size: 14px;
    padding: 8px 10px;
    color: #fff;
    height: 36px;
    width: 80px;
    vertical-align: middle;
  }

  .login-btn-location{
    width: 90px;
    margin-left: 8px;
  }
  .contribute{
    margin-left: 6%;
    height: 36px;
    width: 80px;
    border-radius: 22px;
  }
  .btn-location{
    display: flex;
    margin-left: 3%;
    margin-top: 2%;
  }

</style>













<!--<template>-->

<!--</template>-->

<!--<script>-->
    <!--export default {-->
        <!--name: "Collection",-->
      <!--data(){-->
          <!--return{-->
            <!--id:this.$route.params.id,-->
            <!--topic:{},-->
            <!--articleList:[],-->
            <!--fansList:[]-->
          <!--}-->
      <!--},-->
      <!--activated(){-->
          <!--this.id = this.$route.params.id-->
      <!--}-->
    <!--}-->
<!--</script>-->

<!--<style scoped>-->

<!--</style>-->
