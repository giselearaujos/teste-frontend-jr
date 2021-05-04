<template>
<div class="container">    
  <div class='wrapper-input'>
    <input class="input" type="text" v-model="search" placeholder="Search Company...">
  </div>
    <div class="row">
      <div class="card" v-for="user in filter" :key="user.id">
        <div class="card-header" >
          <h3>{{user.company.name}}</h3>
        </div>
        <div class="card-body">
          <p><strong>Name: </strong>{{user.name}}</p>          
          <p><strong>Phone: </strong>{{user.phone}}</p>
          <p><strong>E-mail: </strong>{{user.email}}</p> 
          <p><strong>Website: </strong>{{user.website}}</p> 
          <p><strong>Phone: </strong>{{user.phone}}</p>           
          <a href="#" class="btn">Read more</a>
        </div>
      </div>       
    </div>
</div> 
</template>

<script>
export default {
    
}
</script>

<style scoped>

</style>