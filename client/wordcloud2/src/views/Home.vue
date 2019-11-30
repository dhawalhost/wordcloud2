<template>
  <div>
    <canvas
      id="word_cloud"
      class="word_cloud"
      width="1300px"
      height="700px"
    ></canvas>
  </div>
</template>

<script>
import WordCloud from "wordcloud/src/wordcloud2";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      list: [
        { word: "Web Technologies", freq: 26 },
        { word: "HTML", freq: 20 },
        { word: "CSS", freq: 15 },
        { word: "JavaScript", freq: 15 },
        { word: "Document Object Model", freq: 12 },
        { word: "Web Workers", freq: 12 },
        { word: "XMLHttpRequest", freq: 12 },
        { word: "SVG", freq: 20 },
        { word: "Geolocation", freq: 9 },
        { word: "data attribute", freq: 9 },
        { word: "transform", freq: 9 },
        { word: "transition", freq: 9 },
        { word: "animation", freq: 9 },
        { word: "setTimeout", freq: 7 },
        { word: "Typed Arrays", freq: 7 },
        { word: "@font-face", freq: 15 },
        { word: "FileReader API", freq: 15 },
        { word: "FormData", freq: 15 },
        { word: "IndexedDB", freq: 14 },
        { word: "getUserMedia", freq: 14 },
        { word: "postMassage", freq: 14 },
        { word: "sharemessage", freq: 14 },
        { word: "CORS", freq: 13 },
        { word: "strict mode", freq: 13 },
        { word: "google", freq: 13 },
        { word: "null", freq: 12 },
        { word: "notification", freq: 12 },
        { word: "text-shadow", freq: 12 },
        { word: "data", freq: 12 },
        { word: "displaymodefull", freq: 12 },
        { word: "box-shadow", freq: 11 },
        { word: "linux", freq: 11 },
        { word: "flexbox", freq: 10 },
        { word: "viewpoint", freq: 10 },

        { word: "function", freq: 10 },

        { word: "titlexdx", freq: 8 },
        { word: "postid", freq: 8 },
        { word: "httpblogpulipuliinfo", freq: 8 },
        { word: "posts", freq: 8 },
        { word: "twitter", freq: 8 },
        { word: "pinterest", freq: 8 },
        { word: "blog", freq: 8 },
        { word: "facebook", freq: 8 },
        { word: "comments", freq: 8 },
        { word: "machine", freq: 7 },
        { word: "chinese", freq: 6 },
        { word: "standalone", freq: 5 },
        { word: "environment", freq: 5 },
        { word: "ubuntu", freq: 5 },
        { word: "password", freq: 5 },
        { word: "rs", freq: 5 },
        { word: "ssh", freq: 5 },
        { word: "draws", freq: 5 },
        { word: "sans", freq: 4 },
        { word: "mining", freq: 4 },
        { word: "stringnoto", freq: 4 }
      ]
    };
  },
  mounted() {
    // var can = document.getElementById("word_cloud");
    // console.log(window.innerWidth);
    // can.style.width = window.innerWidth + "px";
    // // can.style.height = window.innerHeight + "px";
    // setTimeout(function() {
    //   can.style.height = window.innerHeight + "px";
    // }, 0);
    // console.log(WordCloud);
    // WordCloud.minFontSize = "500px";
    // console.log(WordCloud.minFontSize);
    let newlist = [];
    for (var i in this.list) {
      newlist.push([this.list[i]["word"], this.list[i]["freq"]]);
    }
    WordCloud(document.getElementById("word_cloud"), {
      list: newlist,
      gridSize: 18,
      weightFactor: 3,
      fontFamily: "Fredoka One,cursive",
      color: "random-dark",
      // hover: window.drawBox,
      // click: function(item) {
      //   alert(item[0] + ": " + item[1]);
      // },
      backgroundColor: "#fff"
    });
  }
};
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@font-face {
  font-family: "Fredoka One";
  font-style: normal;
  font-weight: normal;
  src: url("../../public/fonts/fredoka-one.woff2") format("woff2");
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
