<template>
  <div class="pl display-flex align-items-center" id="search-container">
    <i class="bx bx-search" id="search-icon"></i>
    <input
      type="text"
      class="form-field"
      id="search-field"
      placeholder="Search"
    />
  </div>
</template>
<style scoped>
#search-container {
  position: relative;
}
#search-field {
  padding-left: 2rem !important;
}

#search-icon {
  position: absolute;
  left: 2rem;
}
</style>
