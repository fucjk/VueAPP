<script type="text/babel">
    import {PaletteButton,Button,MessageBox } from 'mint-ui';
    export default {
        components:{
            [PaletteButton .name]:PaletteButton,
            [Button.name]:Button,
            [MessageBox .name]:MessageBox
        }
    }
</script>

<style lang="scss">
    form{ padding: 0.6rem }
    .mint-button--large{ width: 100%;margin: 1rem auto;font-size: 0.7rem;color: #ffffff;background-color: #ff7212;}
    form .list { height: 2rem }
    form .list span{ line-height: 2rem }
    form .upload { background-color: #ff7212;color: #ffffff;float: right }
</style>

<template>
    <form>
        <p>价格图片(选填)</p>
        <mt-palette-button content="+" @expand="main_log('expand')" @expanded="main_log('expanded')" @collapse="main_log('collapse')"
                           direction="rt" class="pb" :radius="80" ref="target_1" mainButtonStyle="color:#fff;background-color:#26a2ff;"
                           style="left:5px;">
            <div class="my-icon-button indexicon icon-popup" @touchstart="sub_log(1)"></div>
            <div class="my-icon-button indexicon icon-popup" @touchstart="sub_log(2)"></div>
            <div class="my-icon-button indexicon icon-popup" @touchstart="sub_log(3)"></div>
        </mt-palette-button>
        <div class="list">
            <span>造价清单:</span>
            <mt-button size="small" class="upload">上传</mt-button>
        </div>
        <mt-button size="large">提交</mt-button>
    </form>
</template>