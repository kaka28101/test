<template>
    <div class="row">
        <div class="col-md-6 col-md-offset-3">
          <div class="panel panel-default">
            <div class="panel-body">
                <div class="form-group">
                    <input
                        v-model="email"
                        class="form-control"
                        type="email"
                        placehoder="Email">
                </div>
                    <input
                        v-model="password"
                        class="form-control"
                        type="password"
                        placehoder="Password">
                </div>
                <button @click="login" class="btn btn-success pull-right">Login</button>
            </div>
          </div>  
        </div>

    </div>
</template>
<script>
    import Vue from 'vue';
    import vueResource from 'vue-resource';

Vue.use(vueResource);
    export default {
        data () {
            return {
                email: '',
                password: ''
            }
        },
        methods: {
            login () {
                var data = {
                    client_id: 2,
                    client_secret: '3vhVSQ47Ij77fwfBZp2yqM3iBnVVPUsBpMa7McLf',
                    grant_type: 'password',
                    username: this.email,
                    password: this.password
                }

                this.$http.post("http://localhost:8000/oauth/token", data)
                    .then(response => {
                        console.log(response)
                    })

                    
                /*.then(function (response){
                    console.log(response)
                })*/
                
            }
        }
    }
    
</script>
<style lang="">
    
</style>