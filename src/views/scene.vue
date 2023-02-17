<template>
  <div class="card-list" ref="content">
    <a-row :gutter="[16, 16]">
      <a-col v-for="item in dataSource" class="gutter-row" :span="6">
        <template>
          <a-card hoverable>
            <template slot="actions" class="ant-card-actions">
              <a-icon key="eye" type="eye" />
              <a-icon key="edit" type="edit" />
              <a-icon key="delete" type="delete" />
            </template>
            <a-card-meta :title="item.title" :description="item.desc">
            </a-card-meta>
          </a-card>
        </template>
      </a-col>
    </a-row>
  </div>
</template>

<script>

const dataSource = []
for (let i = 0; i < 12; i++) {
  dataSource.push({
    title: `场景名称${i + 1}`,
    desc: `性状组合${i + 1}`
  })
}


export default {
  name: "CardList",
  data() {
    return {
      dataSource
    }
  }
}
</script>

<style lang="less" scoped>
.card-list {
  padding: 10px;
}
</style>