<template>
  <div>
    <el-button v-on:click="visible=true" >ダイアログを開く</el-button>
    <el-dialog v-bind:visible.sync="visible" title="確認">
      <p>Try Element</p>
    </el-dialog>
  </div>
</template>
<script>
export default {
    data: function(){
        return {
            visible: false
        }
    }
}    
</script>


