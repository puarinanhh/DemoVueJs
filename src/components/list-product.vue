<template>
    <div>
        <!-- <div class="test">
            <a>{{testBindding}}</a>
            <input v-model="testBindding" />
        </div> -->
        <a-form :layout="formLayout" :label-col="{ span: 5 }" :wrapper-col="{ span: 12 }">
            <a-form-item label="Tìm kiếm">
                <a-input type="text" name="search" v-model="searchProduct123" v-on:keyup="searchProduct" placeholder="Tìm kiếm">                   
                </a-input>
            </a-form-item>
        </a-form>
        <!-- <div class="form-group">
            <input type="text" name="search" v-model="searchProduct123" placeholder="Tìm sản phẩm" class="form-control" v-on:keyup="searchProduct">
        </div> -->
        <div id="list-product">
            <a-table :columns="columns" :data-source="listProduct">
                <a slot="name" slot-scope="text">{{ text }}</a>
                <span slot="action">
                    <a>Edit</a>
                    <a-divider type="vertical" />
                    <a>Delete</a>
                </span>
            </a-table>
        </div>
    </div>
</template>

<script>
const columns = [
    {
        title: 'ID',
        dataIndex: 'id',
        key: 'id',
    },
    {
        title: 'Name',
        dataIndex: 'name',
        key: 'name'
    },
    {
        title: 'Price',
        dataIndex: 'price',
        key: 'price'
    },
    {
        title: 'Action',
        dataIndex: 'action',
        key: 'action',
        scopedSlots: { customRender: 'action' },
    }
];
    export default {
        data(){
            return {
            formLayout: 'horizontal',
            testBindding: 'Hằng xinh gái',
            columns,
            listProduct: [
                {id: 1, name: "Sản phẩm A", price: 30000}
            ],
            }
            
        },
        methods: {
            searchProduct: function() {

            }
        },
    }
</script>

<style lang="scss" scoped>

</style>