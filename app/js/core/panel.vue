<template>
    <section class="[panelclss,cname]">
        <h4>-{{title}}-</h4>
        <slot/>
    </section>
</template>
<script>
export default{
    data(){
        return {
            panelclss:'panel'
        }
    },
    props:{
        cname:{
            type:String,
            default:''
        },
        title:{
            type:String,
            default:''
        }
    }
}  
</script>
<style lang="scss">
    @import "../../css/element.scss"
    .panel{
        @include panel;
    }
</style>