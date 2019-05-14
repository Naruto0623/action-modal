<template>
  <div>
    <Modal v-model="isShow" width="360">
      <p slot="header">
        <span v-html="mTitle"></span>
      </p>
      <div>
        <p v-html="mText"></p>
      </div>
      <div slot="footer">
        <Button type="dashed" size="small" @click="openModal(2)">{{ buttonCancel }}</Button>
        <Button type="error" size="small" @click="actionOk">{{ buttonOk }}</Button>
      </div>
    </Modal>
  </div>
</template>

<script>
  export default {
    name: "actionModal",
    data(){
      return {
        //模态框是否显示
        isShow: false,
      }
    },
    props: {
      //模态框标题
      mTitle: {
        type: String,
        default: '删除确认'
      },
      //模态框提示内容
      mText: {
        type: String,
        default: '是否删除此数据？'
      },
      //模态框取消按钮字
      buttonCancel: {
        type: String,
        default: '取消'
      },
      //模态框确认按钮字
      buttonOk: {
        type: String,
        default: '删除'
      }
    },
    methods: {
      //打开或者关闭模态框 1为打开，2为关闭
      openModal( num = 1 ){
        if (num == '1') {
          this.isShow = true;
        } else {
          this.isShow = false;
        }
      },
      actionOk(){
        this.$emit('deletePost');
      }
    }
  }
</script>
