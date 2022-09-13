<template>
    <div class="step-container">
        <div class="step-wrap" v-for="(item, index) in steps" :key="item.value">
            <img :src="item.img">
            <span>{{ item.name }}</span>
            <div v-if="index !== steps.length - 1" :class="{'active':isActive, 'divider': !isActive}"></div>
        </div>
    </div>
</template>
<script>
export default {
    props: ['steps', 'activite'],
    data(){
        return {
            isActive: false
        }
    }
}
</script>
<style scoped>
.step-container,
.step-wrap {
    display: flex;
    align-items: center;
}
.divider {
    width: 164px;
    height: 1px;
    background-color: #CCD0D9;
}
.active {
    background-color: #000;
}
</style>