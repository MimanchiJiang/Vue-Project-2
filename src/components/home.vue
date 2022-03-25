<template>
  <transition name="guodu1">
    <div>
      <div class="div_h">
        <img src="../assets/lunbo/home.jpg" alt="" class="img_h" />
      </div>

      <div>
        <introduce></introduce>
      </div>
      <div>
        <iconarea></iconarea>
      </div>
    </div>
  </transition>
</template>
<script>
import introduce from "@/components/homechild/introduce";
import iconarea from "@/components/homechild/iconarea";

export default {
  data() {
    return {};
  },
  methods: {},
  components: {
    introduce,
    iconarea,
  },
};
</script>
<style>
/* home */
.img_h {
  width: 100%;
  height: 610px;
}
.div_h {
  position: relative;
}

.next_h {
  position: absolute;
  width: 50px;
  height: 50px;
  left: 650px;
  top: 430px;
  cursor: pointer;
  opacity: 0.4;
  transition: 1s;
}
.next_h:hover {
  opacity: 0.7;
}
/* 介绍 */
.jieshao {
  width: 100%;
  height: 190px;
  box-sizing: border-box;
}
.fenge1,
.fenge2 {
  width: 300px;
}
.fenge1 {
  float: left;
  margin-left: 185px;
}
.fenge2 {
  float: right;
  margin-right: 200px;
}
.content {
  margin-top: 30px;
}
.span1 {
  margin-left: 65px;
  font-size: 22px;
  font-weight: 700;
}
.p1 {
  margin-left: 528px;
}
.p2 {
  margin-left: 515px;
  font-size: 18px;
  font-weight: 500;
}
.guodu1-enter,
.guodu-fade1-leave-active {
  opacity: 0;
}
.guodu1-enter-active,
.guodu1-leave-active {
  transition: opacity 1s ease;
}
</style>

