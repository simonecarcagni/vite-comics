<script>
export default {
    name: "TheFooter",
    data() {

    },

}

</script>

<template>
    <footer>
        <div class="footer-top">
            <div class="container"></div>
        </div>
        <div class="footer-bottom">
            <div class="container ms_space_between">
                <div class="button-container">
                    <button> SIGN-UP NOW!</button>
                </div>
                <div class="followus-container">
                    <h5>FOLLOW US</h5>
                    <div>icon</div>
                    <div>icon</div>
                    <div>icon</div>
                    <div>icon</div>
                    <div>icon</div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins";

.footer-top {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    height: 400px;
}

.footer-bottom {
    height: 100px;
    background-color: $color-bg-footer;
}

.ms_space_between {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.followus-container {
    @include mixins.d-flex-center;
}
</style>
