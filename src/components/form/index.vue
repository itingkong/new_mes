<template>
  <div class="form">
    <p class="form_title">{{title}}</p>
    <table-item :tableData="tableData" :labelList="labelList" class="table"></table-item>
  </div>
</template>

<script>
import TableItem from '@/components/table'
export default {
  components: {
    TableItem,
  },
  props: {
    tableData: Array,
    labelList: Array,
    title: String
  },
  data() {
    return {
      
    }
  },
  mounted() {
    
  },
  methods: {

  }
}
</script>

<style lang="stylus" scoped>
  .form 
    height 100%
    width 100%
    border 1px solid #eee
    border-radius 4px
    &_title
      height 40px
      line-height 40px
      font-weight 700
      font-size 18px
      color #333
      margin 0
      border-bottom 1px solid #eee
</style>
