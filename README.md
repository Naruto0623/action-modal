# action-modal

> actionModal

## Installing

```bash
$ npm install action-modal --save
```

## Useing
#### introduce in the Js

```bash
import actionModal from 'action-modal';
```

#### introduce in the Vue

```bash
<template>
  <action-modal 
      ref="actionModal"
      :mTitle='删除确认'
      :mText='是否删除此数据'
      :buttonCancel='取消'
      :buttonOk='删除'
      @actionOk="myActionFn">
  </action-modal>
</template>
```
## Invoking method 

```bash
//open
this.$refs.actionModal.openModal();
//close
this.$refs.actionModal.openModal(2);
```

## Props

#### mTitle：

模态框标题，默认值为：删除确认，可不传

#### mText：

模态框显示内容文字，默认值为：是否删除此数据，可不传，支持html

#### buttonCancel：

模态框取消按钮显示文字，默认值为：取消，可不传

#### buttonOk：

模态框确认操作按钮显示文字，默认值为：删除，可不传

## Event

#### @actionOk：

点击确认后的回调函数，触发父组件自定义函数

For detailed explanation on how things work, consult the [docs for action-modal](https://github.com/Naruto0623/action-modal).
