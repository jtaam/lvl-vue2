<template lang="html">
  <div class="row">
    <div class="col-md-6 col-md-offset-3">
      <div class="panel panel-default">
        <div class="panel-body">
          <div class="form-group">
            <input v-model="email" type="email" class="form-control" id="" placeholder="Email">
          </div>
          <div class="form-group">
            <input v-model="password" type="password" name="" value="" class="form-control" placeholder="Password">
          </div>
          <!-- /.form-group -->
          <button @click='test' class="btn btn-success pull-right">Login</button>
        </div>
        <!-- /.panel-body -->
      </div>
      <!-- /.panel panel-default -->
    </div>
    <!-- /.col-md-6 col-md-offset-3 -->
  </div>
  <!-- /.row -->
</template>

<script>
export default {
  data(){
    return {
      email:'',
      password:''
    }
  },
  methods:{
    test(){
      this.$http.get("http://127.0.0.1:8000/api/test")
        .then(function(response){
          console.log(response);
        })
    }
  }
}
</script>

<style lang="css">
</style>
