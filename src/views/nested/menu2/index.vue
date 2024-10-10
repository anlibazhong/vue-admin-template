<template>
  <div class="app-container">
    <el-form ref="form" :model="form" label-width=" 200px">
      <el-form-item label="Stock_Classes">
        <el-radio-group v-model="form.class">
          <el-radio label="Common Stock" />
          <el-radio label="Preferred Stock"/>
          <el-radio label="Dual-Class Shares" />
          <el-radio label="Employee Stock Ownership" />
        </el-radio-group>
      </el-form-item>
      <el-form-item label="Stock Price">
        <el-input v-model="form.price" />
      </el-form-item>
      <el-form-item label="Shareholder Base">
        <el-radio-group v-model="form.shareholder">
          <el-radio label="Common ShareHolder" />
          <el-radio label="Preferred ShareHolder" />
          <el-radio label="Institution Investors" />
          <el-radio label="Individual Investors" />
          <el-radio label="Inside ShareHolder" />
          <el-radio label="Founding Shareholds" />
        </el-radio-group>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit">Broadcast</el-button>
        <el-button @click="onCancel">Cancel</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        class: '',
        shareholder: '',
        price: ''
      }
    }
  },
  methods: {
    onSubmit() {
      this.$message('submit!')
    },
    onCancel() {
      this.$message({
        message: 'cancel!',
        type: 'warning'
      })
    }
  }
}
</script>

<style scoped>
.line{
  text-align: center;
}
</style>


