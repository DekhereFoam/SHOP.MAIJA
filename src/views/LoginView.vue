<template>
    <div class="container my-5">
      <div class="row justify-content-center">
        <div class="col-md-6">
          <div class="card shadow p-4">
            <h2 class="text-center mb-4">เข้าสู่ระบบ</h2>
            <form @submit.prevent="handleLogin">
              <div class="mb-3">
                <label class="form-label">ชื่อผู้ใช้ หรือ อีเมล</label>
                <input type="text" class="form-control" v-model="form.usernameOrEmail" required>
              </div>
              <div class="mb-3">
                <label class="form-label">รหัสผ่าน</label>
                <input type="password" class="form-control" v-model="form.password" required>
              </div>
              <button type="submit" class="btn btn-success w-100">เข้าสู่ระบบ</button>
            </form>
            <div class="text-center mt-3">
              <p>ยังไม่มีบัญชี? <a href="signup">สมัครสมาชิก</a></p>
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
          usernameOrEmail: '',
          password: ''
        }
      };
    },
    methods: {
      handleLogin() {
        console.log('เข้าสู่ระบบด้วย:', this.form);
        alert('เข้าสู่ระบบสำเร็จ! เริ่มช้อปเลย...');
        this.form = { usernameOrEmail: '', password: '' };
        this.$router.push('/'); // 🔥 หลังล็อกอินเสร็จพาไปหน้าหลัก
      }
    }
  }
  </script>
  
  <style scoped>
  h2 {
    font-weight: bold;
  }
  </style>
  