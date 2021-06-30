<template>
        <div class="menu_srch d-flex">
            <i class="fa fa-search search_btn" @click="showSearch = !showSearch"></i>
            <!-- SEARCH INPUT  dis_none-->
            <div class="header_serch " @click.stop v-if="showSearch">
                <div class="header_serch_input">
                    <input type="text" v-model="str" @keyup.enter="searchBlog" placeholder="Search">
                </div>
                <div class="header_serch_i" >
                    <i class="fa fa-search"></i>
                </div>
            </div>
            <!-- SEARCH INPUT -->
        </div>
</template>

<script>
export default {
    data() {
        return {
            showSearch : false,
            str: ''
        }
    },
    methods: {
        searchBlog() {
            window.location = `/search?str=${this.str}`
        }
    },
created() {
    console.log('here we go...')
}
}
</script>

<style>

</style>