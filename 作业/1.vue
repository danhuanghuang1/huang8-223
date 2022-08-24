<template>
  <div>
    <ul>
      <li v-for="(p, index) in person" :key="index">
        {{ p }}
      </li>
    </ul>
    <!-- 点击按钮调整li的排序方式 -->
    <button @click="sortArr">走一走</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      person: ["帅哥", "美女", "程序猿"],
    };
  },
  methods: {
    sortArr() {
      // 把数组的第一项放到最后
      this.person.push(this.person[0]);
      // 再把第一项删除
      this.person.shift();
    },
  },
};
</script>

<style></style>
