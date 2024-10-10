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
      <el-form-item label="Declaration Data">
          <el-date-picker v-model="form.date1" type="date" placeholder="Pick a date" style="width: 100%;" />
      </el-form-item>
      <el-form-item label="Ex-Divident Data">
          <el-date-picker v-model="form.date2" type="date" placeholder="Pick a date" style="width: 100%;" />
      </el-form-item>
      <el-form-item label="Record Data">
          <el-date-picker v-model="form.date3" type="date" placeholder="Pick a date" style="width: 100%;" />
      </el-form-item>
      <el-form-item label="Payment Data">
          <el-date-picker v-model="form.date4" type="date" placeholder="Pick a date" style="width: 100%;" />
      </el-form-item>
      <el-form-item label="Note">
        <el-input v-model="form.name" />
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
        class: '',
        name: '',
        region: '',
        date1: '',
        date2: '',
        date3: '',
        date4: '',
        delivery: false,
        type: [],
        resource: '',
        desc: ''
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

