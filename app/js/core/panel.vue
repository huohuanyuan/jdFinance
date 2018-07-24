/*
 * @Author: chengshanshan 
 * @Date: 2018-07-19 11:27:12 
 * @Last Modified by: chengshanshan
 * @Last Modified time: 2018-07-19 11:32:53
 */
 
<template>
    <section :class=[panelClass,cname]>
        <h4>-{{title}}-</h4>
        <slot></slot>
    </section>
</template>
<script>
export default {
    props:{
        cname:{
            type:"String",
            default:""
        },
        title:{
            type:"String",
            default:""
        }
    },
    data() {
        return {
            panelClass:"panel"
        }
    }
}
</script>
<style lang="scss" scoped>
@import "../../css/element.scss";
.panel{
    @include panel();
}

</style>