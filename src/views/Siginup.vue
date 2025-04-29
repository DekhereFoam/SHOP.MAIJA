<template>
    <div class="container my-5">
      <div class="row justify-content-center">
        <div class="col-md-6">
          <div class="card shadow p-4">
            <h2 class="text-center mb-4">สมัครสมาชิก</h2>
            <form @submit.prevent="handleSignup">
              <div class="mb-3">
                <label class="form-label">ชื่อผู้ใช้</label>
                <input type="text" class="form-control" v-model="form.username" required>
              </div>
              <div class="mb-3">
                <label class="form-label">อีเมล</label>
                <input type="email" class="form-control" v-model="form.email" required>
              </div>
              <div class="mb-3">
                <label class="form-label">รหัสผ่าน</label>
                <input type="password" class="form-control" v-model="form.password" required>
              </div>
              <button type="submit" class="btn btn-primary w-100">สมัครสมาชิก</button>
            </form>
            <div class="text-center mt-3">
              <p>มีบัญชีอยู่แล้ว? <a href="login">เข้าสู่ระบบ</a></p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        form: {
          username: '',
          email: '',
          password: ''
        }
      };
    },
    methods: {
      handleSignup() {
        console.log('สมัครสมาชิก:', this.form);
        alert('สมัครสมาชิกเรียบร้อย! เริ่มช้อปเลย...');
        this.form = { username: '', email: '', password: '' };
        this.$router.push('/'); // 🔥 ใช้ router เด้งไปหน้าหลัก
      }
    }
  }
  </script>
  
  <style scoped>
  h2 {
    font-weight: bold;
  }
  </style>
  
  