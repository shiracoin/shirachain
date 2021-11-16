<template>
  <h1>Shira Explorer</h1>
<div>
<div class="latest_block item1">
    <div class="header">
        <div class="title">
            <h2 class="txt">Block Info</h2>
        </div>
    </div>
  <div class="block_list">
    
        <ul class="item title">
            <li class="inner_item height">Height</li>
            <li class="inner_item">Hash</li>
            <li class="inner_item size">Size (Bytes)</li>
            <li class="inner_item">Diff</li>
            <li class="inner_item">Tx Count</li>
            <li class="inner_item time">Time</li>
            <li class="inner_item">Pool</li>
        </ul>
        <span v-for="block in blocks" :key="block.id">
        
            <ul class="item content">
                <li class="inner_item height">
                <router-link :to="{ name: 'BlockDetails', params: { id: block.height }}">
                {{ block.height }}       
                </router-link>
                </li>
                <li class="inner_item">
                <router-link :to="{ name: 'BlockDetails', params: { id: block.height }}">
                {{ block.hash }}       
                </router-link>
                </li>
            <li class="inner_item size">Size</li>
            
            <li class="inner_item">Diff</li>
            <li class="inner_item">Tx Count</li>
            <li class="inner_item time">Time</li>
            <li class="inner_item">Pool</li>

            </ul>
        </span>
  </div>
</div>
</div>
</template>

<script>
export default {
    data() {
        return {
            blocks: []
        }
    },
    async mounted()
    {
        // let shira = await axios.get('http://192.168.0.102:4444/api/listsinceblock');
        // console.warn(shira.data.result)
        // this.blocks = shira.data.result
    }
}
</script>

<style scoped>
.latest_block {
    font-family: Roboto-Regular,Helvetica Neue,Helvetica,Hiragino Sans GB,STHeitiSC-Light,Microsoft YaHei,\5FAE软雅黑,Arial,sans-serif;
    width: 100%;
    max-width: 1200px;
    height: auto;
    min-height: 250px;
    margin: 16px auto;
    border-radius: 4px;
    background-color: #fff;
    border: 1px solid #d2d7e1;
    overflow: hidden;
    position: relative;
    padding-bottom: 58px;
}
article, aside, blockquote, body, button, dd, details, div, dl, dt, fieldset, figcaption, figure, footer, form, h1, h2, h3, h4, h5, h6, header, hgroup, hr, input, legend, li, menu, nav, ol, p, section, td, textarea, th, ul {
    margin: 0;
    padding: 0;
}
.block_list {
    width: 100%;
    height: auto;
}
.block_list .title .inner_item {
    font-size: 14px;
    color: #8e9ab5;
}
.block_list .item {
    width: 100%;
    height: 58px;
    padding: 0 14px 0 19px;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-pack: justify;
    -ms-flex-pack: justify;
    justify-content: space-between;
    border-bottom: 1px solid #eeeff1;
    background: #fff;
}
li {
    list-style: none;
}
.block_list .item .height, .block_list .item .miner {
    width: 9%;
}
.block_list .item .size {
    text-align: right;
}
.latest_block .header {
    width: 100%;
    height: 50px;
    background-color: #fff;
    padding: 0 14px 0 19px;
}
.latest_block .header .title {
    overflow: hidden;
    width: auto;
    height: 100%;
    float: left;
}
.latest_block .header .title .txt {
    float: left;
    line-height: 50px;
    font-size: 16px;
    color: #213654;
    overflow: hidden;
}
.mobileList{display:none}.block_list{width:100%;height:auto}.block_list .item{width:100%;height:58px;padding:0 14px 0 19px;display:-webkit-box;display:-ms-flexbox;display:flex;-webkit-box-pack:justify;-ms-flex-pack:justify;justify-content:space-between;border-bottom:1px solid #eeeff1;background:#fff}.block_list .item .inner_item{float:left;font-size:14px;color:#213654;width:12%;margin-right:10px;text-overflow:ellipsis;overflow:hidden;white-space:nowrap}.block_list .item .height,.block_list .item .miner{width:9%}.block_list .item .gas{width:15%;text-align:right}.block_list .item .gas div{white-space:nowrap;overflow:hidden;text-overflow:ellipsis}.block_list .item .gas .rate{color:#8e9ab5}.block_list .item .size{text-align:right}.block_list .item .prize{width:15%;text-align:right}.block_list .item .num{width:10%;text-align:right}.block_list .item .amount{width:18%;text-align:right}.block_list .item .hash{width:40%}.block_list .title{height:32px;line-height:32px;background:#f4f5f8}.block_list .title .inner_item{font-size:14px;color:#8e9ab5}.block_list .content{display:-webkit-box;display:-ms-flexbox;display:flex;-webkit-box-align:center;-ms-flex-align:center;align-items:center}.block_list .content .miner{color:#213654}.block_list .content .miner a{color:#438ef7}.ru .block_list .title{height:auto;line-height:1;overflow:hidden;padding:10px 14px 10px 19px}.ru .block_list .title .inner_item{font-size:14px;font-weight:600;text-overflow:unset;overflow:unset;white-space:unset}.grin .block_list .item .inner_item{width:25%}@media screen and (max-width:500px){.mobileList{display:block;background:#fff}.mobileList .items{padding:15px 10px;border-bottom:1px solid #eeeff1}.mobileList .items .item{display:-webkit-box;display:-ms-flexbox;display:flex;-webkit-box-align:baseline;-ms-flex-align:baseline;align-items:baseline;font-size:12px;margin:5px 0}.mobileList .items .item .key{color:#8e9ab5;min-width:93px;width:93px}.mobileList .items .item .value{color:#213654;overflow:hidden;text-overflow:ellipsis}.mobileList .items .item .value a{display:block;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}.block_list{display:none;overflow:auto}.block_list .title{min-width:600px}.block_list .item{min-width:600px;height:31px;line-height:31px}.block_list .item .inner_item{height:auto;font-size:11px}}
</style>