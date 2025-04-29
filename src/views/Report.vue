<template> 
  <nav class="navbar navbar-expand-lg navbar-light bg-white shadow-sm sticky-top">
    <div class="container">
      <a class="navbar-brand fw-bold text-dark" href="#">
        <img src="../assets/shoplogo.png" alt="Logo" width="80" height="80" class="d-inline-block align-text-mid me-2">
        SHOP.MAIJA | wherehouse
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <a class="nav-link active fw-semibold" href="/">หน้าแรก</a>
          </li>
          <li class="nav-item">
            <a class="nav-link fw-semibold" href="about">หมวดหมู่</a>
          </li>
          <li class="nav-item">
            <a class="nav-link fw-semibold" href="pro">โปรโมชั่น</a>
          </li>
          <li class="nav-item">
            <a class="nav-link fw-semibold" href="me">เกี่ยวกับ</a>
          </li>
          <li class="nav-item">
            <a class="nav-link fw-semibold " href="report">รายงานปัญหา</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- ส่วนฟอร์มรายงานปัญหา -->
  <div class="container my-5">
    <h1 class="text-center mb-4 text-danger">รายงานปัญหา</h1>
    <div class="card p-4 shadow-sm">
      <form @submit.prevent="submitForm">
        <div class="mb-3">
          <label for="name" class="form-label">ชื่อของคุณ</label>
          <input type="text" class="form-control" id="name" v-model="form.name" required>
        </div>
        <div class="mb-3">
          <label for="email" class="form-label">อีเมล</label>
          <input type="email" class="form-control" id="email" v-model="form.email" required>
        </div>
        <div class="mb-3">
          <label for="message" class="form-label">ข้อความถึงเรา</label>
          <textarea class="form-control" id="message" rows="5" v-model="form.message" required></textarea>
        </div>
        <button type="submit" class="btn btn-primary w-100">ส่งข้อความ</button>
      </form>
    </div>
  </div>

  <footer class="py-3 my-4">
    <ul class="nav justify-content-center border-bottom pb-3 mb-3">
      <li class="nav-item"><a href="/" class="nav-link px-2 text-body-secondary">หน้าแรก</a></li>
      <li class="nav-item"><a href="about" class="nav-link px-2 text-body-secondary">หมวดหมู่</a></li>
      <li class="nav-item"><a href="pro" class="nav-link px-2 text-body-secondary">โปรโมชั่น</a></li>
      <li class="nav-item"><a href="me" class="nav-link px-2 text-body-secondary">เกี่ยวกับ</a></li>
      <li class="nav-item"><a href="report" class="nav-link px-2 text-body-secondary">รายงานปัญหา</a></li>
    </ul>
    <p class="text-center text-body-secondary">© 2025 Company, Inc</p>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      }
    }
  },
  methods: {
    submitForm() {
      console.log('ส่งข้อมูล:', this.form);
      alert('ขอบคุณสำหรับการรายงานปัญหา! เราจะติดต่อกลับโดยเร็วที่สุด');
      this.form = { name: '', email: '', message: '' }; // รีเซ็ตฟอร์ม
    }
  }
}
</script>

<style scoped>
h1 {
  font-weight: bold;
}
</style>
