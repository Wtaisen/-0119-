<template>
    <div>
        <h1>Parent组件</h1>
        <!-- 使用子组件 步骤3：调用组件 -->
        <child1 :inpmsg="pmsg" @sendmsg="getVal"></child1>
        <div>
            接收进来的数据为：{{incmsg}}
        </div>
    </div>
</template>
<script>
//使用子组件 步骤1：导入child组件
import child1 from './Child.vue'
export default {
    //使用子组件 步骤2 ：注册子组件
    components:{
        child1
    },data(){
        return {
            pmsg:'父的data',
            incmsg:''
        }
    },
    methods: {
        getVal(inmsg){
            this.incmsg = inmsg;
        }
    },
}
</script>