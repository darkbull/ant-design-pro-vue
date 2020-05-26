<template>
  <a-card :bordered="false">
    <a-table :columns="columns" :dataSource="data" :defaultExpandAllRows="true" :indentSize="30">
      <span slot="name"><b>Name</b></span>
      <!-- <span slot="name2" slot-scope="text">{{ text }}</span> -->
    </a-table>
  </a-card>
</template>
<script>
  export default {
    data () {
      return {
        columns: [
          {
            key: 'name',
            dataIndex: 'name',
            // title: 'Name',
            slots: {
              title: 'name'
            }
            // scopedSlots: {
            //   customRender: 'name2'
            // },
          },
          {
            key: 'age',
            dataIndex: 'age',
            title: 'Age'
          },
          {
            key: 'action',
            slots: {
              title: ''
            }
          }
        ],
        data: [
          {
            name: 'Kim',
            age: 18,
            children: [{ name: 'Leeast', age: 22 }]
          },
          {
            name: 'Join',
            age: 22
          }
        ]
      }
    }
  }
</script>
