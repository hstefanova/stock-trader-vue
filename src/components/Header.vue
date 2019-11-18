<template>
    <div class="header">
        <div class="header__inner">
            <div class="header__content">
                <Navigation></Navigation>
            </div>

            <div class="header__aside">
                <NavUtilities></NavUtilities>
            </div>
        </div>
    </div>
</template>

<script>
import Navigation from './Navigation'
import NavUtilities from './NavUtilities'

export default {
    components: {
        Navigation,
        NavUtilities
    }
}
</script>

<style lang="scss" scope>
    .header {
        background: #eee; 

        .header__inner {
            display: flex;
            width: 100%;
            justify-content: space-between;
        }
    }
</style>

