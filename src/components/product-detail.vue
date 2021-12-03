<template>
    <div>
        <form id="app" @submit="submitForm" method="post">
            <p>
                <label for="id">ID</label>
                <input type="text" id="id" name="id" disabled="true" v-model="product.id">
            </p>
            <p>
                <label for="name">Name</label>
                <input type="text" id="name" name="name" v-model="product.name">
            </p>
            <p>
                <label for="price">Price</label>
                <input type="number" id="price" name="price" v-model="product.price">
            </p>
            <p>
                <input type="submit" value="Submit">
            </p>
        </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                product: {
                    id: null,
                    name: null,
                    price: null,
                }            
            }
        },
        methods: {
            submitForm: function(){
                
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>