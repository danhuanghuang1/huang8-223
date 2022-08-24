<template>
  <div>
    <thead>
      <tr>
        <td>编号</td>
        <td>品牌名称</td>
        <td>创立时间</td>
        <td>操作</td>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(p, index) in person" :key="index">
        <td>
          {{ p.id }}
        </td>
        <td>
          {{ p.name }}
        </td>
        <td>
          {{ p.time }}
        </td>
        <td><button @click="del(index)">删除</button></td>
      </tr>
    </tbody>
      <tr v-if="person.length === 0">
        <td colspan="4">没有数据咯~</td>
      </tr>
  </div>
</template>

<script>
export default {
  data() {
    return {
      person: [
        {
          id: 1,
          name: "奔驰",
          time: "2020-08-01",
        },
        {
          id: 2,
          name: "宝马",
          time: "2020-08-02",
        },
        {
          id: 3,
          name: "奥迪",
          time: "2020-08-03",
        },
      ],
    };
  },
  methods: {
    del(index) {
      this.person.splice(index, 1);
    },
  },
};
</script>

<style scoped>
td{
  padding: 5px 30px;
  border: 1px solid black;
  text-align: center;
}
thead{
  background-color: #0094ff;
}
</style>
