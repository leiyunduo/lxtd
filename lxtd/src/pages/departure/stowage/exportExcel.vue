<template><!-- 王艺蒙 -->
  <el-button class="emportcss" id="yin" size="mini">
    <form class="yinc" :action="url" method="post">
        <input type="text" :value="data" name="table" class="hidecla">
        <input type="text" :value="1020" class="hidecla" name="pageId">
        <input type="submit" value="导出装载申请表" class="ess" />
    </form>
  </el-button>
</template>

<script>
import { baseUrl } from '@/config/env.js'
export default {
  props: ["data"],
  data() {
    return {
      url: baseUrl + "/develop_tool/table2Excel",
      pageId: 1020,
    }
  },
}
</script>

<style lang="less">
  .ess{
    height: 32px;
    padding:7px 15px;
    font-size: 12px;
    border-radius: 6px;
    background: #8768FF;
    border-color: #8768FF;
    color: #fff;
    white-space: nowrap;
    cursor: pointer;
    text-align: center;
    box-sizing: border-box;
    outline: 0;
    margin: 0;
    border:none;
  }
  #yin{
    background:#e9eef3!important;
    border: 0px solid #d8dce5!important;
  }
  .hidecla{
    display:none !important;
  }
  .yinc{
    background:rgba(2,2,2,0)
  }
  .emportcss{
    padding:0;
    background:#e9eef3!important;
    border: 0px solid #d8dce5!important;
  }
</style>

