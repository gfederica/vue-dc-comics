<template>

<footer>
    <div class="pre-footer"></div>
    <div class="navigate"></div>
    <div class="sign-up-bar"></div>
</footer>


</template>
<script>


export default {
    name: 'Footer'
}
</script>
<style scoped lang="scss">

@import "../style/general.scss";

.pre-footer {
    height: 150px;
    background-color: $blueColor;
}
.navigate {
    height: 310px;
    background-image: url($footerBackground);
}
.sign-up-bar {
    height: 10vh;
    background-color: $greyColorFooterBg;
}

</style>
