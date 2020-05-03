<template>
    <div class="bili-button" :class="buttonType" @click="onClick">
        <slot>
            button
        </slot>
    </div>
</template>


<script lang="ts">
import{Component,Vue,Prop,Emit}from 'vue-property-decorator';

@Component
export default class BiliButton extends Vue{

    @Prop() private type:string | undefined;

    @Emit('click')
    private emitClickEvent(event:MouseEvent){}

    private onClick(event:MouseEvent){
        this.emitClickEvent(event);
    }

    get buttonType (){
        if(this.type==undefined){
            return 'default'
        }

        return this.type  
    }
}
</script>
 
<style lang="scss" scope>
.bili-button{
    font-size:14px;
    display:inline-block;
} 
</style>