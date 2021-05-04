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
.container {
  width: 90%;
  margin: 50px auto;
}

.wrapper-input {
  display: flex;
  justify-content: center;  
}

.input {
  width: 30%;
  margin-bottom: 50px;
  border-radius: 15px;
  padding:15px;
  color: #180F50;
  font-size: 16px;
  font-weight: bold;
}

.row {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  flex-flow: wrap;
}

.card {
  width: 20%;
  background: #fff;
  border: 1px solid #ccc;
  border-radius: 15px;
  margin-bottom: 50px;
  transition: 0.3s;
}

.card-header {
  text-align: center;
  padding: 50px 10px;
  background: linear-gradient(to right, #180f50b6,#3113f2b2,#3d9ef2af);
  border-radius: 15px 15px 0px 0px;
  color: #fff;
}

.card-body {
  padding: 30px 20px;
  text-align: left;
  font-size: 14px;
}

.card-body .btn {
  display: block;
  color: #fff;
  text-align: center;
  background: linear-gradient(to right,#180f50ad,#3113f2ab,#3d9ef2ab);
  border-radius: 15px;
  margin-top: 30px;
  text-decoration: none;
  padding: 10px 5px;
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0 0 40px -10px rgba(0, 0, 0, 0.363);
}

@media screen and (max-width: 1000px) {
  .card {
    width: 40%;
  }
}

@media screen and (max-width: 620px) {
  .container {
    width: 100%;
  }
  .card {
    width: 80%;
  }
  .input {
    width: 70%;
  }
}
</style>