<template>
  <div class="app-container">
    
    <!-- Navigation Container -->
    <div class="nav-container">
      <!-- Logo -->
      <div class="logo-container">
        <img src="/images/logo_nav.png" alt="Logo" class="logo" />
      </div>

      <!-- Links Container -->
      <div class="links-container">
       <!-- Patients' Access -->
       <div class="nav-item">
          <a class="nav-title">Patients’ Access</a>
        </div>

        <!-- Doctors' Access and Blogs -->
        <div class="nav-group">
          <!-- Doctors' Access -->
          <div class="nav-item">
            <div class="nav-title">Doctors’ Access</div>
          </div>

          <!-- Blogs -->
          <div class="nav-item" >
            <div class="nav-title">Blogs</div>
          </div>

          <!-- Language Selector -->
          <div class="language-selector">
            <select
              v-model="selectedLanguage"
              @change="handleChange"
              class="custom-select"
            >
              <option value="en">En</option>
              <option value="french">French</option>
            </select>
          </div>
        </div>
      </div>
    </div>

    <!-- Custom Design Element -->
    <div class="custom-design-container">
      <!-- Custom Design Elements using absolute positioning -->
      <div
        v-for="(element, index) in customDesignElements"
        :key="index"
        :style="element.style"
        class="custom-design-element"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      customDesignElements: [
        {
          width: "15.98px",
          height: "21.60px",
          left: "0px",
          top: "4px",
          background: "#01B7C4",
        },
        {
          width: "4.94px",
          height: "22.49px",
          left: "18.58px",
          top: "3.10px",
          background: "#01B7C4",
        },
      ],
      selectedLanguage: 'en',
    };
  },
  
};
</script>

<style scoped>
.app-container {
  width: 100%;
  height: 100%;
  position: relative;
}

.nav-container {
  display: flex;
  align-items: center;
  padding: 0 20px;
  box-sizing: border-box;
}

.logo-container {
  margin-right: 24px;
}

.logo {
  width: 100%;
  height: auto;
}

.links-container {
  flex-grow: 1;
  display: flex;
  justify-content: flex-end;
}

.nav-item {
  position: relative;
  height: 35px;
  padding: 10px;
  justify-content: space-between;
  align-items: flex-start;
  display: flex;
  cursor: pointer;
  transition: border-bottom 0.3s ease-in-out;
}

.nav-title:hover{
  color: #01B7C4;
  border-bottom: 1px #01B7C4 solid;

}

.nav-group {
  justify-content: flex-start;
  align-items: flex-start;
  gap: 24px;
  display: flex;
}

.nav-title {
  color: #000000;
  font-size: 16px;
  font-family: Raleway;
  font-weight: 600;
  word-wrap: break-word;
}

.language-selector {
  margin-left: 10px;
}

.custom-select {
  border: 1px solid #303532;
  /* Border color */
  border-radius: 20px;
  /* Rounded corners */
  padding: 8px;
  /* Padding inside the select */
  font-size: 16px;
  font-family: Raleway;
  color: #303532;
  background-color: #F8F8F8;
}

.custom-design-container {
  width: 100%;
  height: 25.97px;
  position: absolute;
}

.custom-design-element {
  position: absolute;
  background: #01b7c4;
}

/* Responsive Styles */
@media screen and (max-width: 600px) {
  .nav-container {
    flex-direction: column;
    align-items: flex-start;
  }

  .logo-container {
    margin-bottom: 10px;
    margin-right: 0; /* Remove right margin for better spacing */
  }

  .links-container {
    justify-content: flex-start;
  }
}

</style>
