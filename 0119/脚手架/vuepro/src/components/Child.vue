<template>
    <div>
        <h1>Child组件</h1>
        <div>
            接收到父传的值为：{{inpmsg}}
        </div>
        <button @click="fn">传递数据</button>
    </div>
</template>
<script>
export default {
    //接收父的数据
    props:["inpmsg"],
    data(){
        return {
            cmsg:'子的data'
        }
    },
    methods: {
        fn(){
            console.log("111");
            this.$emit("sendmsg",this.cmsg);
        }
    },
}
</script>