<template>
  <div class="profile-card">
    <div class="profile-image">
      <img src="~/static/profile.jpg" alt="Foto do Perfil" />
    </div>
    <div class="profile-info">
      <h2>Seu Nome</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
        Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris...
      </p>
    </div>
  </div>
</template>

<style scoped>
.profile-card {
  display: flex;
  align-items: center;
  max-width: 100%;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
  box-sizing: border-box;
  background-color: #c0c0c0;
}

.profile-image {
  width: 100px;
  height: 100px;
  overflow: hidden;
  border-radius: 50%;
  margin-right: 20px;
}

.profile-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.profile-info {
  flex: 1;
}

.profile-info h2 {
  margin-bottom: 10px;
}

.profile-info p {
  line-height: 1.6;
  margin: 0;
}
</style>
