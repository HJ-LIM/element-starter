<template>
  <div class="container">
    <div>
      <el-radio v-model="radio" label="1" disabled>Option A</el-radio>
      <el-radio v-model="radio" label="2">Option 2</el-radio>
    </div>
    <div>
      <el-radio-group v-model="radio2" size="mini">
        <el-radio label="3" border>Option A</el-radio>
        <el-radio label="6">Option B</el-radio>
        <el-radio label="9">Option C</el-radio>
      </el-radio-group>
    </div>
    <div>
      <el-checkbox-group v-model="checkList">
        <el-checkbox label="Option A"></el-checkbox>
        <el-checkbox label="Option B"></el-checkbox>
        <el-checkbox label="Option C"></el-checkbox>
        <el-checkbox label="disabled" disabled></el-checkbox>
        <el-checkbox label="selected and disabled" disabled></el-checkbox>
      </el-checkbox-group>
    </div>
    <div>
      <el-checkbox :indeterminate="isIndeterminate" v-model="checkAll" @change="handleCheckAllChange">Check All</el-checkbox>
      <div style="margin: 15px 0;"></div>
      <el-checkbox-group v-model="checkedCities" @change="handleCheckedCitiesChange">
        <el-checkbox v-for="city in cities" :label="city" :key="city">{{city}}</el-checkbox>
      </el-checkbox-group>
    </div>
  </div>

</template>

<script>


import ElRadio from "../node_modules/element-ui/packages/radio/src/radio.vue";

const cityOptions = ['Shanghai', 'Beijing', 'Guangzhou', 'Shenzhen'];
export default {
    components: {
        ElRadio
    },
    methods: {
        handleCheckAllChange(val){
            this.checkedCities = val ? cityOptions : [];
            this.isIndeterminate = false;
        },
        handleCheckedCitiesChange(value){
            console.debug(this);
            console.debug(value);
            let checkedCount = value.length;
            this.checkAll = checkedCount === this.cities.length;
            this.isIndeterminate = checkedCount > 0 && checkedCount < this.cities.length;
        }
    },
    data(){
        return{
            radio:'2',
            radio2 :'9',
            checkList:['selected and disabled' , 'Option A'],
            checkAll : false,
            checkedCities : ["Shanghai" , "Beiging"],
            cities : cityOptions,
            isIndeterminate : true
        }
    },


}
</script>

<style>
  .container{
    width: 1200px;
    margin: 150px auto 0;
  }

</style>
