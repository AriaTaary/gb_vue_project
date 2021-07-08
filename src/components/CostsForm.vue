<template>
    <el-form ref="form" :model="form" label-width="120px">
        <el-form-item>
            <label for="category">Категория:</label>
            <el-input id="category" v-model="form.category"></el-input>
        </el-form-item>
        <el-form-item>
            <label for="value">Значение:</label>
            <el-input id="value" v-model="form.value"></el-input>
        </el-form-item>
        <el-form-item>
            <label for="date">Дата:</label>
            <el-input id="date" type="date" v-model="form.date"></el-input>
        </el-form-item>
        <el-form-item>
            <button class="add-button" type="button" @click="onSubmit">Создать</button>
        </el-form-item>
    </el-form>
</template>

<script>
  export default {
    props: {
        costs: Array,
    },
    data() {
      return {
        form: {
          id: '',  
          category: '',
          value: '',
          date: '',
        }
      }
    },
    methods: {
      onSubmit() {
        this.form.id = this.costs.length + 1;
        this.$emit('updateCosts', this.form);
      }
    }
  }
</script>