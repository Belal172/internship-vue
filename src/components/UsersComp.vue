<template>
<h2>user component</h2>
<h3>{{ ram }}</h3>
<div class="users">
    <h2 v-for="item in users" :key="item.email">{{ item.email }}</h2>
</div>
</template>

<script>
export default {
    name: 'UserComp',
    props: {
        users: Object,
        ram: String
    }
}
</script>

<style scoped>
.users {
    gap: 3px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #f9f9f9;
}
</style>
