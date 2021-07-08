<template>
    <el-table class="costs_table"
        :data="sortCosts"
        style="width: 100%">
        <el-table-column
        prop="id"
        label="#"
        width="50">
        </el-table-column>
        <el-table-column
        prop="date"
        label="Дата"
        width="180">
        </el-table-column>
        <el-table-column
        prop="category"
        label="Категория">
        </el-table-column>
        <el-table-column
        prop="value"
        label="Значение">
        </el-table-column>
    </el-table>
</template>

<script>

export default {
    props: {
        sortCosts: Array,
    },
}
</script>