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
            <a class="nav-link fw-semibold" href="report">รายงานปัญหา</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  
  <div class="px-4 py-5 my-5 text-center">
  <h1 class="display-5 fw-bold  text-danger"> HOT โปรโมชั่น !! </h1>

  <div class="container mb-5">
<div class="row row-cols-1 row-cols-md-3 g-4">
  <div class="col">
    <div class="card h-100 shadow-sm">
      <img src="../assets/pic1.jpg" class="card-img-top" alt="เสื้อเชิ้ตลินินคอจีน">
      <div class="card-body">
        <h5 class="card-title">เสื้อยืด 7 th colection ดำ </h5>
      </div>
      <div class="card-footer">
        <small class="text-danger fw-bold">ราคา: 450 บาท  จาก 650 บาท </small>
      </div>
      
    </div>
  </div>

  <div class="col">
    <div class="card h-100 shadow-sm">
      <img src="../assets/pic4.jpg" class="card-img-top" alt="กระโปรงสั้นพลีท">
      <div class="card-body">
        <h5 class="card-title">กางเกง 8 th colection ดำ</h5>
      </div>
      <div class="card-footer">
        <small class="text-danger fw-bold">ราคา: 890 บาท 1 แถมฟรี กระบอกน้ำ 35 oz.</small>
      </div>
    </div>
  </div>

  <div class="col">
    <div class="card h-100 shadow-sm">
      <img src="../assets/pic6.webp" class="card-img-top" alt="เสื้อไหมพรมคอเต่า">
      <div class="card-body">
        <h5 class="card-title">รองเท้า Street black air2</h5>
      </div>
      <div class="card-footer">
        <small class="text-danger fw-bold">ราคา: 2,580 บาท จาก 2,950 บาท</small>
      </div>
    </div>
  </div>
</div>
</div>






<a href="/" class="btn btn-primary " tabindex="-1" role="button" >กลับ</a>





</div>

  
<footer class="py-3 my-4 bg-light position-relative">
  <div class="container text-center">
    <!-- รูปภาพที่จะเปลี่ยนไปเรื่อยๆ -->
    <img
      :src="currentImage"
      class="img-fluid rounded shadow mb-4"
      alt="Footer Image"
      style="max-width: 300px; height: 300;"
    />

    <!-- ลิงก์ใน Footer -->
    <ul class="nav justify-content-center border-top pt-3 mt-3">
      <li class="nav-item"><a href="/" class="nav-link px-2 text-muted">หน้าแรก</a></li>
      <li class="nav-item"><a href="/about" class="nav-link px-2 text-muted">หมวดหมู่</a></li>
      <li class="nav-item"><a href="/pro" class="nav-link px-2 text-muted">โปรโมชั่น</a></li>
      <li class="nav-item"><a href="/me" class="nav-link px-2 text-muted">เกี่ยวกับ</a></li>
      <li class="nav-item"><a href="/report" class="nav-link px-2 text-muted">รายงานปัญหา</a></li>
    </ul>
    <p class="text-muted mt-2">© 2025 Company, Inc</p>
  </div>
</footer>

  
  </template>
  <script>
  export default {
    data() {
      return {
        images: [
          require('@/assets/bbbb.png'), // ใส่รูปที่ 1 ที่คุณมี
          require('@/assets/SHop.png')  // ใส่รูปที่ 2 ที่คุณมี
        ],
        currentImageIndex: 0,
        intervalId: null
      };
    },
    computed: {
      currentImage() {
        return this.images[this.currentImageIndex];
      }
    },
    mounted() {
      this.startImageRotation();
    },
    beforeUnmount() {
      clearInterval(this.intervalId);
    },
    methods: {
      startImageRotation() {
        this.intervalId = setInterval(() => {
          this.currentImageIndex = (this.currentImageIndex + 1) % this.images.length;
        }, 3000); // เปลี่ยนรูปทุก 3 วินาที
      }
    }
  }
  </script>
  
  
  