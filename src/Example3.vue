<template>
  <!--<el-container>-->
    <!--<el-header>Header</el-header>-->
    <!--<el-main>Main</el-main>-->
    <!--<el-footer>Footer</el-footer>-->
  <!--</el-container>-->
  <el-container style="height: 500px; border:1px solid #eee;">
    <el-aside width="200px" style="background-color:rgb(238,241,246)">
      <el-menu :default-openeds="['1','3']">
        <el-submenu index="1">
          <template slot="title"><i class="el-icon-message"></i>Navigator One</template>
          <el-menu-item-group>
            <template slot="title">Group 1</template>
            <el-menu-item index="1-1">Option 1</el-menu-item>
            <el-menu-item index="1-2">Option 2</el-menu-item>
          </el-menu-item-group>
          <el-menu-item-group title="Group 2">
            <el-menu-item index="1-3">Option 3</el-menu-item>
          </el-menu-item-group>
          <el-submenu index="1-4">
            <template slot="title">Option4</template>
            <el-menu-item index="1-4-1">Option 4-1</el-menu-item>
          </el-submenu>
        </el-submenu>
        <el-submenu index="2">
          <template slot="title"><i class="el-icon-menu"></i>Navigatory Two</template>
          <el-menu-item-group>
            <template slot="title">Group 1</template>
            <el-menu-item index="2-1">Option 1</el-menu-item>
            <el-menu-item index="2-2">Option 2</el-menu-item>
          </el-menu-item-group>
          <el-menu-item-group title="Group 2">
            <el-menu-item index="2-3">Option 3</el-menu-item>
          </el-menu-item-group>
          <el-submenu index="2-4">
            <template slot="title">Option 4</template>
            <el-menu-item index="2-4-1">Option 4-1</el-menu-item>
          </el-submenu>
        </el-submenu>
        <el-submenu index="3">
          <template slot="title"><i class="el-icon-setting"></i>Navigator Three</template>
          <el-menu-item-group>
            <template slot="title">Group 1</template>
            <el-menu-item index="3-1">Option 1</el-menu-item>
            <el-menu-item index="3-2">Option 2</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
      </el-menu>
    </el-aside>
    <el-container>
      <el-header style="text-align: right; font-size: 12px">
        <el-dropdown>
          <i class="el-icon-setting" style="margin-right:15px;"></i>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>View</el-dropdown-item>
            <el-dropdown-item>Add</el-dropdown-item>
            <el-dropdown-item>Delete</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
        <span>Tom</span>
      </el-header>

      <el-main>
        <el-table :data="tabelData">
          <el-table-column prop="date" label="date" width="140">
          </el-table-column>
          <el-table-column prop="date" label="date" width="120">
          </el-table-column>
          <el-table-column prop="address" label="Address">
          </el-table-column>
        </el-table>

      </el-main>
    </el-container>
  </el-container>


</template>

<script>

import ElContainer from "../node_modules/element-ui/packages/container/src/main.vue";
import ElHeader from "../node_modules/element-ui/packages/header/src/main.vue";
import ElFooter from "../node_modules/element-ui/packages/footer/src/main.vue";
import ElAside from "../node_modules/element-ui/packages/aside/src/main.vue";
import ElSubmenu from "../node_modules/element-ui/packages/menu/src/submenu.vue";
import ElMenuItemGroup from "../node_modules/element-ui/packages/menu/src/menu-item-group.vue";
import ElMenuItem from "../node_modules/element-ui/packages/menu/src/menu-item.vue";
import ElDropdownMenu from "../node_modules/element-ui/packages/dropdown/src/dropdown-menu.vue";
import ElDropdownItem from "../node_modules/element-ui/packages/dropdown/src/dropdown-item.vue";

export default {
    components: {
        ElDropdownItem,
        ElDropdownMenu,
        ElMenuItem,
        ElMenuItemGroup,
        ElSubmenu,
        ElAside,
        ElFooter,
        ElHeader,
        ElContainer
    },
    methods: {

    },
    data(){
        const item ={
            date : '2017-12-22',
            name : 'Tom',
            address : 'No.189'
        };

        return {
            tabelData : Array(20).fill(item)
        }
    }

}
</script>

<style>
  .el-header {
    background-color: #B3C0D1;
    color: #333;
    line-height: 60px;
  }

  .el-aside {
    color: #333;
  }
</style>
