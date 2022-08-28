
<script setup>
import {ref} from 'vue'

defineProps({
  msg: String
})

const count = ref(0)
</script>

<template>

  <div class="head fix">
    <div class="t1 fix">
<!--      <div class="tl"><a href="" target="_self">Hello | World</a></div>-->
      <!-- support.html -->
      <div class="tr">
        <ul class="ur">
          <li><a href="index.html">首页</a></li>
        </ul>
      </div>
    </div>

    <div class="tt">
      <div class="t2">笔记</div>
      <div class="t3">记录生活中的点点滴滴</div>
    </div>
  </div>
  <div class="content">
    <div class="item">
      <div class="text_en"><a>只要不失去你的崇高，整个世界都会为你敞开。</a></div>
      <div class="text_en">
        一直想有一个属于自己的网站，存放自己的学习笔记，记录生活中的点点滴滴，伴随着我的成长
        <br>于是，我的代码之旅从此开始...<br><br>
        <br>由于时间有限，笔记还只是冰山一角，会在今后补充！<br><br>
<!--        <div align="right">-->
<!--&lt;!&ndash;          printf("Helloworld\n");&ndash;&gt;-->
<!--&lt;!&ndash;          <br>&ndash;&gt;-->
<!--        </div>-->
      </div>
<!--      <div class="text_en">Posted on 2022</div>-->
    </div>

  </div>


  <footer style="text-align:center;">
    <a href="https://beian.miit.gov.cn" rel="external nofollow" target="_blank">豫ICP备2022017315号-2</a>
  </footer>


</template>

<script>
!function () {
  function n(n, e, t) {
    return n.getAttribute(e) || t
  }

  function e(n) {
    return document.getElementsByTagName(n)
  }

  function t() {
    var t = e("script"), o = t.length, i = t[o - 1];
    return {l: o, z: n(i, "zIndex", -1), o: n(i, "opacity", .5), c: n(i, "color", "0,0,0"), n: n(i, "count", 99)}
  }

  function o() {
    a = m.width = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth, c = m.height = window.innerHeight || document.documentElement.clientHeight || document.body.clientHeight
  }

  function i() {
    r.clearRect(0, 0, a, c);
    var n, e, t, o, m, l;
    s.forEach(function (i, x) {
      for (i.x += i.xa, i.y += i.ya, i.xa *= i.x > a || i.x < 0 ? -1 : 1, i.ya *= i.y > c || i.y < 0 ? -1 : 1, r.fillRect(i.x - .5, i.y - .5, 1, 1), e = x + 1; e < u.length; e++) n = u[e], null !== n.x && null !== n.y && (o = i.x - n.x, m = i.y - n.y, l = o * o + m * m, l < n.max && (n === y && l >= n.max / 2 && (i.x -= .03 * o, i.y -= .03 * m), t = (n.max - l) / n.max, r.beginPath(), r.lineWidth = t / 2, r.strokeStyle = "rgba(" + d.c + "," + (t + .2) + ")", r.moveTo(i.x, i.y), r.lineTo(n.x, n.y), r.stroke()))
    }), x(i)
  }

  var a, c, u, m = document.createElement("canvas"), d = t(), l = "c_n" + d.l, r = m.getContext("2d"),
      x = window.requestAnimationFrame || window.webkitRequestAnimationFrame || window.mozRequestAnimationFrame || window.oRequestAnimationFrame || window.msRequestAnimationFrame || function (n) {
        window.setTimeout(n, 1e3 / 45)
      }, w = Math.random, y = {x: null, y: null, max: 2e4};
  m.id = l, m.style.cssText = "position:fixed;top:0;left:0;z-index:" + d.z + ";opacity:" + d.o, e("body")[0].appendChild(m), o(), window.onresize = o, window.onmousemove = function (n) {
    n = n || window.event, y.x = n.clientX, y.y = n.clientY
  }, window.onmouseout = function () {
    y.x = null, y.y = null
  };
  for (var s = [], f = 0; d.n > f; f++) {
    var h = w() * a, g = w() * c, v = 2 * w() - 1, p = 2 * w() - 1;
    s.push({x: h, y: g, xa: v, ya: p, max: 6e3})
  }
  u = s.concat([y]), setTimeout(function () {
    i()
  }, 100)
}();
</script>
<style scoped>
@import "../css/common.css";
@import "../css/home.css";
@import "../css/translate-card.css";
</style>
