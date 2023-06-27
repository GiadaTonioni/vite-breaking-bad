<script>
export default {

}
</script>
<template lang="">
    <div class="container">
        <div class="row">
            <div class="col">
                <div class="circle1"></div>
                <div class="circle2"></div>
                <div class="circle3"></div>
                <div class="circle4"></div>
            </div>
        </div>
        

    </div>
</template>
<style lang="scss" scoped>
.circle1 {
    background-color: rgb(63, 63, 255);
    border-radius: 50%;
    border: 3px solid black;
    height: 80px;
    width: 80px;
    margin-top: 50px;
    display: inline-block;
}

.circle2,
.circle3,
.circle4 {
    border-radius: 50%;
    border: 3px solid black;
    height: 50px;
    width: 50px;
    display: inline-block;
    margin-left: 10px;
    margin-bottom: 30px;
}

.circle2 {
    background-color: rgb(255, 95, 95);
}

.circle3 {
    background-color: rgb(255, 255, 110);
}

.circle4 {
    background-color: rgb(107, 255, 107);
}
</style>