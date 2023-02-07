
<template>
    <VNavigationDrawer permanent app class="primary lighten-2">
        <v-container grid-list-xs>
            <v-col height="fill-height">
                <v-row cols="12" justify="center">
                    <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="">
                </v-row>
                <v-row cols="12" justify="center" class="text-sm-center">
                    <h2 class="background--text">{{sName}}</h2>
                </v-row>
            </v-col>
        </v-container>
    </VNavigationDrawer>
</template>

<script>
    export default {
        props: ["sName"],
        name: 'Drawer',
        drawer: null
    }
</script>

<style lang="scss" scoped>
img{
    border-radius: 100px;
}

</style>