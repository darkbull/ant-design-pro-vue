<template>
  <a-card :bordered="false">
    <a-badge :count="999"><a href="#" class="head-class">Fuck</a></a-badge>
    <br />
    <a-badge :count="33" status="success" text="just test"></a-badge>
  </a-card>
</template>

<script>
export default {
}
</script>

<style>
.head-class {
  display: block;
  padding: 5px;
  font-size: 14px;
  background-color: #eee;
  line-height: 25px;
  border-radius: 5pt;
}
</style>
