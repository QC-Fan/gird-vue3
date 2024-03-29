<template>
    <el-button type="primary" @click="handleButtonClick(params)">新增</el-button>
</template>
<script setup>
function handleButtonClick(params) {
    console.log(params);
    // params.colDef.colSpan = row => {
    //     return 6;
    // };
    // 合并第2列和第3列



}
</script>
<style scoped></style>