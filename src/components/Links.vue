<script>
export default {
    name: 'Links',
    props: ['linkInfo']
}
</script>

<template>

 
    <a class="nav-link" :href="linkInfo.path">{{ linkInfo.label }}</a>


</template>

<style scoped lang="scss">

 a {
    color: black;
 }

</style>