<template>
  <div class='flex flex-row'>
    <el-button class='mr-2' type="danger" @click="clearOpts">清空选项</el-button>
    <el-select
      v-model="opt"
      value-key="id"
      @change="handleChange"
      filterable
      clearable
      remote
      :remote-method="remoteMethod"
      placeholder="请输入选项"
    >
      <el-option
        v-for="(item, i) in opts"
        :key="i"
        :label="item.label"
        :value="item"
      >
        <div>
          {{ item.label }}
        </div>
      </el-option>
      <template #header>
        <el-button size="small" type="primary">添加选项</el-button>
      </template>
      <template #empty>
        <el-button size="small" type="primary">添加选项</el-button>
      </template>
    </el-select>
  </div>
</template>

<script setup lang="ts">
const opts = ref([
  {
    id: 1,
    label: "选项1",
    payload: {
      name: "xxx",
      age: 18,
    },
  },
]);
const opt = ref<any>();
const clearOpts = () => {
  opts.value = [];
};
const handleChange = (val: any) => {
  console.log(val);
};
const remoteMethod = (query: string) => {
  console.log(query);
};
</script>

<style scoped></style>
