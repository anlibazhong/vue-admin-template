<template>
  <div class="app-container">
    <el-form ref="form" :model="form" label-width=" 200px">
      <el-form-item label="Company Overview">
        <el-input v-model="form.overview" />
      </el-form-item>
      <el-form-item label="Financial Information">
        <el-input v-model="form.financial" />
      </el-form-item>
      <el-form-item label="Management Information">
        <el-input v-model="form.management" />
      </el-form-item>
      <el-form-item label="Use of Proceeds">
        <el-input v-model="form.use" />
      </el-form-item>
      <el-form-item label="Risk Factors">
        <el-input v-model="form.risk" />
      </el-form-item>
      <el-form-item label="Offering Terms">
        <el-input v-model="form.offering" />
      </el-form-item>
      <el-form-item label="Legal and Regulatory Information">
        <el-input v-model="form.legal" />
      </el-form-item>
      <el-form-item label="Price">
        <el-input v-model="form.price" />
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit">Create</el-button>
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
        overview: '',
        financial: '',
        management: '',
        use: '',
        legal: '',
        risk: '',
        offering: '',
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

