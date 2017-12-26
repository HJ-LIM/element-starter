<template>
  <div class="container">
    <div>
      <el-button>Default</el-button>
      <el-button type="primary" round >Primary</el-button>
      <el-button type="success" disabled>Primary</el-button>
      <el-button type="info" plain >Primary</el-button>
      <el-button type="warning" plain round disabled>Primary<i class="el-icon-upload"></i></el-button>
      <el-button type="danger" icon="el-icon-search">Primary</el-button>
    </div>
    <div>
      <el-button type="text">Text Button</el-button>
      <el-button type="text" disabled>Text Button</el-button>
    </div>

    <div>
      <el-button-group>
        <el-button type="primary" icon="el-icon-arrow-left" round>Previous Page</el-button>
        <el-button type="success" round>Next Page<i class="el-icon-arrow-right"></i></el-button>
      </el-button-group>
    </div>
    <div>
      <el-button type="primary" :loading="false" native-type="submit">Loading</el-button>
      <el-button type="primary" :loading="false" size="medium">Loading</el-button>
      <el-button type="primary" :loading="false" size="small">Loading</el-button>
      <el-button type="primary" :loading="false" size="mini">Loading</el-button>
    </div>
  </div>

</template>

<script>

import ElButton from "../node_modules/element-ui/packages/button/src/button.vue";
import ElButtonGroup from "../node_modules/element-ui/packages/button/src/button-group.vue";

export default {
    components: {
        ElButtonGroup,
        ElButton
    },
    methods: {

    }

}
</script>

<style>

</style>
