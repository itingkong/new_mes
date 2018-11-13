<template>
  <div class="home">
    <h3>We will create a new world, great one.</h3>
    <div class="form_wrap">
      <form-item :tableData="tableData" :labelList="labelList" :title="title"></form-item>
      <form-item :tableData="tableData2" :labelList="labelList2" :title="title2"></form-item>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import FormItem from '@/components/form'

export default {
  name: 'home',
  components: {
    HelloWorld,
    FormItem
  },
  data() {
    return {
      title: 'shift',
      title2: 'machine',
      labelList: [
        {id: 0, label: '班次ID', prop: 'shiftId', labelWidth: '120',type:'select'},
        {id: 1, label: '班次CODE', prop: 'shiftCode', labelWidth: '120' ,type:'select',rules:"required"},
        {id: 2, label: '班次名称', prop: 'shiftName', labelWidth: '120' ,type:'input'},
        {id: 3, label:'方案ID',prop:'projectsId',labelWidth:'120',tableShow:false},
        {id: 4, label:'方案CODE',prop:'projectsCode',labelWidth:'120'},
        {id: 5, label:'租户ID',prop:'tenantId',labelWidth:'120',tableShow:false},
        {id: 6, label:'租户CODE',prop:'tenantCode',labelWidth: '120'},
        {id: 7, label: '是否有效数据', prop: 'activeFlag', labelWidth: '120' },
        {id: 8, label: '更新时间', prop: 'updateTime', labelWidth: '120' },
        {id: 9, label: '更新人员', prop: 'updatePerson', labelWidth: '120' }
      ],
      labelList2: [
        {id:0,label:'设备ID',prop:'machineId',labelWidth:'120',type:'input'},
        {id:1,label:'设备代码',prop:'machineCode',labelWidth:'120',type:'input',rules:"required",fixed: 'left'},
        {id:2,label:'中文名称',prop:'nameCn',labelWidth:'120',type:'input'},
        {id:3,label:'英文名称',prop:'nameEn',labelWidth:'120',type:'input'},
        {id:4,label:'简码，别名',prop:'nameShort',labelWidth:'120',type:'input'},
        {id:5,label:'设备组ID',prop:'machineGroupId',labelWidth:'120',type:'select',tableShow:false},
        {id:6,label:'设备组CODE',prop:'machineGroupCode',labelWidth:'120'},
        {id:7,label:'设备当前状态',prop:'machineState',labelWidth:'120',type:'select'},
        {id:8,label:'设备类别',prop:'machineType',labelWidth:'120',type:'select'}
      ],
      tableData: [
        {
          shiftId: '001',
          shiftCode: 'code001',
          shiftName: 'name001',
          projectsId: '方案001',
          projectsCode: '方案Code001',
          tenantId: '租户001',
          tenantCode: '租户Code001',
          activeFlag: '是',
          updateTime: '2018-11-12',
          updatePerson: 'luoqi'
        },{
          shiftId: '002',
          shiftCode: 'code002',
          shiftName: 'name002',
          projectsId: '方案002',
          projectsCode: '方案Code002',
          tenantId: '租户002',
          tenantCode: '租户Code002',
          activeFlag: '是',
          updateTime: '2018-11-12',
          updatePerson: 'luoqi'
        },{
          shiftId: '003',
          shiftCode: 'code003',
          shiftName: 'name003',
          projectsId: '方案003',
          projectsCode: '方案Code003',
          tenantId: '租户003',
          tenantCode: '租户Code003',
          activeFlag: '是',
          updateTime: '2018-11-12',
          updatePerson: 'luoqi'
        }
      ],
      tableData2: [
        {
          machineId: '001',
          machineCode: 'code001',
          nameCn: '南山',
          nameEn: 'southMountain',
          nameShort: 'sm',
          machineGroupId: '南001',
          machineGroupCode: '南Code001',
          machineState: 'acitve',
          machineType: 'super'
        },{
          machineId: '002',
          machineCode: 'code002',
          nameCn: '桃花岛',
          nameEn: 'island',
          nameShort: 'i',
          machineGroupId: '桃001',
          machineGroupCode: '桃Code001',
          machineState: 'acitve',
          machineType: 'superSuper'
        },{
          machineId: '003',
          machineCode: 'code003',
          nameCn: '古墓',
          nameEn: 'home',
          nameShort: 'h',
          machineGroupId: '古003',
          machineGroupCode: '古Code003',
          machineState: 'acitve',
          machineType: 'peace'
        }
      ],
    }
  }
}
</script>

<style lang="stylus" scoped>
  .home
    .form_wrap
      width 100%
      height 100%
      display flex
      align-items center
      justify-content space-around
      >div {
        width 45%
      }
</style>
