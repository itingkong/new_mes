<template>
  <el-table
    class="elTable"
    :data="tableData"
    style="width: 100%"
    height="570px">
    <el-table-column
      type="selection"
      header-align="center"
      align="center"
      width="50"
      fixed="left">
    </el-table-column>
    <el-table-column
      type="index"
      width="50"
      align="center"
      label="序号"
      fixed="left">
    </el-table-column>
    <el-table-column
      v-for="(item, i) in labelList"
      :key="i"
      align="center"
      fit
      :prop="item.prop"
      :label="item.label">
    </el-table-column>
  </el-table>
</template>

<script>
export default {
  props: {
    tableData: Array,
    labelList: Array,
  },
  data() {
    return {
      
    }
  },
  mounted() {
    console.log('table', this.tableData)
  },
  methods: {

  }
}
</script>

<style lang="stylus" scoped>
  // .elTable
    
</style>
