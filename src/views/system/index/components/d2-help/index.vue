<template>
  <div>
    <el-button type="primary" @click="dialogVisible = true" plain round>
      <d2-icon name="question-circle-o" class="d2-mr-5"/>
      {{ $t('views.system.index.help.button') }}
    </el-button>
    <el-dialog
      :title="$t('views.system.index.help.dialog.title')"
      width="600px"
      :visible.sync="dialogVisible"
      :append-to-body="true">
      <div style="margin-top: -25px; margin-bottom: -25px;">
        <h2 class="d2-mt-0">
          {{ $t('views.system.index.help.dialog.sub-title.doc') }}
        </h2>
        <el-button-group>
          <el-button @click="$open('https://doc.d2admin.fairyever.com/zh/')">
            <d2-icon name="book" class="d2-mr-5"/>
            {{ $t('views.system.index.help.dialog.link.text.doc') }}
          </el-button>
          <el-button @click="$open('https://github.com/d2-projects/d2-admin/issues?q=is%3Aissue+is%3Aclosed')">
            <d2-icon name="question" class="d2-mr-5"/>
            {{ $t('views.system.index.help.dialog.link.text.issues') }}
          </el-button>
          <el-button @click="$open('https://github.com/d2-projects/d2-admin/issues/new/choose')">
            <d2-icon name="plus" class="d2-mr-5"/>
            {{ $t('views.system.index.help.dialog.link.text.new-issue') }}
          </el-button>
        </el-button-group>
        <h2>{{ $t('views.system.index.help.dialog.sub-title.join') }}</h2>
        <el-row :gutter="20">
          <el-col :span="12">
            <el-alert
              :closable="false"
              type="info"
              :title="$t('views.system.index.help.dialog.join.qq')"
              class="d2-mb"/>
            <img src="./image/qq.jpg" style="width: 100%;">
          </el-col>
          <el-col :span="12">
            <el-alert
              :closable="false"
              type="info"
              :title="$t('views.system.index.help.dialog.join.we')"
              class="d2-mb"/>
            <img src="./image/we.jpg" style="width: 100%;">
          </el-col>
        </el-row>
      </div>
    </el-dialog>
  </div>
</template>

<script>
export default {
  data () {
    return {
      dialogVisible: false
    }
  }
}
</script>
