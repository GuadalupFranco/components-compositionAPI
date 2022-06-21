<template>
    <div>{{ user }} Repositories</div>
</template>

<script>
export default {
    props: {
        user: {
            type: String,
            required: true
        },
    },
    setup(props, ctx) {
        return {
            repositories
        }
    },
    data() {
        return {
            repositories: [],
            filters: {},
            searchQuery: "",
        };
    },
    computed: {
        filteredRepositories(){
            return null;
        },
        repositoriesMarchingSearchQuery () {
            return null
        }
    }
}
</script>