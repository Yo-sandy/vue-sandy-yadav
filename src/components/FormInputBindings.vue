<template>
<div class="container m-2">
  <div class="row">
    <div class="col-md-6">
      <div class="mb-3">
        <lable for="email" class="form-label">Email address</lable>
        <input
            type="email"
            v-model="email"
            class="form-control"
            id="email"
            placeholder="name@example.com"
        />
      </div>
      <p>Your Email:{{email}}</p>
      <div class="mb-3">
        <lable for="password" class="form-label">Password</lable>
        <input
            type="password"
            v-model="password"
            class="form-control"
            id="password"
            placeholder="Enter your password"
        />
      </div>
      <p>Your password:{{password}}</p>
      <input
          type="checkbox"
          v-model="select"
          true-value="on"
          false-value="off"
      />
      <p>Select:  {{select}}</p>
      <textarea  class="form-control" v-model="address"></textarea>
      <p>address:{{address}}</p>
      <select class="form-select" v-model="city">
      <option disabled value="">select your city</option>
      <option value="hisar">Hisar</option>
      <option value="hansi">hansi</option>
      <option value="sirsa">sirsa</option>
      <option value="rohtak">rohtak</option>
      </select>
      <p>Your City: {{city}}</p>
      <input type="text" class="form-control mb-2" v-model.number="value1"/>
      <input type="text" class="form-control" v-model.number="value2"/>
      <h5>Your total is :{{sum}}</h5>
    </div>
  </div>
</div>
</template>


<script>
export default {
  data(){
    return{
      email:"",
      password:"",
      select:"",
      address:"",
      city:"",
      value1: 0,
      value2: 0,
    };
  },
  computed: {
    sum(){
      return this.value1 + this.value2;
    },
  },
};
</script>