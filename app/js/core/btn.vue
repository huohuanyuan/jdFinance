/*
 * @Author: chengshanshan 
 * @Date: 2018-07-19 11:10:18 
 * @Last Modified by: chengshanshan
 * @Last Modified time: 2018-07-19 11:16:45
 */

<template lang="html">
    <div :class="[btnClass,cname]">
       <slot></slot>
    </div>
</template>
<script>
export default {
    props:{
        cname:{
            type:String,
            default:""
        }
    },
    data(){
        return {
            btnClass:'btn',

        }
    }
}
</script>
<style lang="scss" scoped>
@import "../../css/element.scss";
.btn{
    @include btn;
}
</style>

