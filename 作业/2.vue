<template>
  <div>
    <ul>
      <li v-for="(p, index) in person" :key="index">
        {{ p }}
        <button @click="del(index)">删除</button>
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
      person: [8, 4, 1],
    };
  },
  methods: {
    sortArr() {
      const num = Math.floor(Math.random() * 50);
      this.person.push(num);
    },
    del(index) {
      this.person.splice(index, 1);
    },
  },
};
</script>

<style></style>
