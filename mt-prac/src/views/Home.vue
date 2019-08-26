<template>
  <div class="home">
    <header>
      <div class="location">广氮商业广场</div>
      <div class="search">
        <input disabled placeholder="请输入商家或商品名称" />
      </div>
    </header>
    <nav>
      <ul class="delitype">
        <a href="/" v-for="(item,index) in this.data" :key="index">
          <li>
            <img :src="item.img" alt />
            <span>生鲜</span>
          </li>
        </a>

        <!-- <li>
          <img src="../assets/fresh.png" alt />
          <span>生鲜</span>
        </li>
        <li>
          <img src="../assets/fresh.png" alt />
          <span>生鲜</span>
        </li>
        <li>
          <img src="../assets/fresh.png" alt />
          <span>生鲜</span>
        </li>
        <li>
          <img src="../assets/fresh.png" alt />
          <span>生鲜</span>
        </li>
        <li>
          <img src="../assets/fresh.png" alt />
          <span>生鲜</span>
        </li>
        <li>
          <img src="../assets/fresh.png" alt />
          <span>生鲜</span>
        </li>
        <li>
          <img src="../assets/fresh.png" alt />
          <span>生鲜</span>
        </li>
        <li>
          <img src="../assets/fresh.png" alt />
          <span>生鲜</span>
        </li>
        <li>
          <img src="../assets/fresh.png" alt />
          <span>生鲜</span>
        </li>-->
      </ul>
    </nav>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
// @import img1 from "../assets/delicious.png";
// @import img2 from "../assets/fresh.png";
// @import img3 from "../assets/specialtran.png";
// @import img4 from "../assets/starchoose.png";
// @import img5 from "../assets/supermarket.png";
// @import img6 from "../assets/delicious.png";
// @import img7 from "../assets/fresh.png";
// @import img8 from "../assets/specialtran.png";
// @import img9 from "../assets/starchoose.png";
// @import img10 from "../assets/supermarket.png";

// import img_location from "@/assets/lcoal.png";
// import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

// @Component({
//   components: {
//     // HelloWorld
//   }
// })
export default class Home extends Vue {
  public data = [
    { img: require('../assets/delicious.png'), txt: '美食' },
    { img: require('../assets/specialtran.png'), txt: '生鲜' },
    { img: require('../assets/starchoose.png'), txt: '专送' },
    { img: require('../assets/supermarket.png'), txt: '下午茶' },
    { img: require('../assets/supermarket.png'), txt: '美团超市' },
    { img: require('../assets/supermarket.png'), txt: '汉堡披萨' },
    { img: require('../assets/supermarket.png'), txt: '小吃馆' },
    { img: require('../assets/supermarket.png'), txt: '家常菜' },
    { img: require('../assets/supermarket.png'), txt: '鲜花蛋糕' },
    { img: require('../assets/supermarket.png'), txt: '品牌连锁' },
  ];
}
</script>
<style lang="less" scoped>
.home {
  header {
    width: 100%;
    height: 50px;
    padding-left: 10px;
    padding-right: 10px;
    box-sizing: border-box;
    background: #1c1b20;
    display: flex;
    align-items: center;
    .location {
      display: flex;
      max-width: 180px;
      // max-width: 0px;
      font-size: 16px;
      align-items: center;
      color: white;
      line-height: 30px;
      overflow: hidden;
      &::before {
        content: "";
        display: inline-block;
        width: 30px;
        height: 30px;
        background: url(../assets/lcoal.png) no-repeat;
        background-size: contain;
      }
      &::after {
        content: "";
        display: inline-block;
        width: 20px;
        height: 20px;
        background: url(../assets/r_arrows.png) no-repeat;
        background-size: contain;
      }
    }
    .search {
      flex: 1;
      background: #ffffff;
      border-radius: 100px;
      height: 30px;
      display: flex;
      align-items: center;
      position: relative;
      input {
        height: 100%;
        border: none;
        width: 100%;
        border-radius: 100px;
        box-sizing: border-box;
        text-overflow: ellipsis;
        padding-right: 30px;
        padding-left: 30px;
        font-size: 14px;
        color: rgb(84, 84, 84);
      }
      &::after {
        content: "";
        display: inline-block;
        width: 15px;
        height: 15px;
        position: absolute;
        left: 10px;
        background: url(../assets/search.png) no-repeat;
        background-size: contain;
      }
    }
  }
  nav {
    ul,
    li {
      list-style: none;
    }
    .delitype {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      padding-right: 20px;
      box-sizing: border-box;
      a {
        display: inline-block;
        text-decoration: none;
        padding-right: 15px;
        // padding-left: 10px;
        margin-bottom: 10px;
        box-sizing: border-box;
        &:nth-child(5),
        &:last-child {
          padding-right: 0;
        }
        li {
          display: flex;
          flex-direction: column;
          align-items: center;

          span {
            color: #333333;
            font-size: 12px;
          }
        }
      }
    }
  }
}
</style>