<template>
    <section class="display">
        {{ valor }}
    </section>
</template>

<script>

export default{
    props: {
        valor: {
            required: true
        }
    }
}

</script>

<style scoped>
 .display{
    display: flex;
    justify-content: end;
    align-items: center;
    widows: 100%;
    height: 12%;
    border: 1px solid white;
    font-size: 35px;
 }
</style>