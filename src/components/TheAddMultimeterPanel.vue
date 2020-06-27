<template>
  <div class="panel panel-primary">
      <div class="panel panel-heading">
          <h4 class="panel-title">Dodaj multimetr</h4>
      </div>
      <div class="panel panel-body">
          <div class="input-group margin-bottom">
              <span class="input-group-addon">Nazwa</span>
              <input type="text" v-model="name" class="form-control" placeholder="Nazwa">
          </div>
          <div class="input-group margin-bottom">
              <span class="input-group-addon">Model</span>
              <input type="text" v-model="model" class="form-control" placeholder="Model">
          </div>
          <div class="row margin-bottom">
              <div class="col-md-6">
                  <div class="input-group margin-bottom">
                      <span class="input-group-addon">Dostępność na magazynie</span>
                      <input type="number" v-model="aviailability" class="form-control" placeholder="Dostępność na magazynie">
                  </div>
              </div>
              <div class="col-md-6">
                  <div class="input-group margin-bottom">
                      <span class="input-group-addon">Stan zużycia</span>
                      <input type="number" v-model="state" class="form-control" placeholder="Stan zużycia">
                  </div>
              </div>
          </div>
          <button
            class="btn btn-danger"
            type="button"
            @click="reset">Resetuj</button>
            &nbsp;
          <button
            class="btn btn-success"
            type="button"
            @click="add">Dodaj</button>
      </div>
  </div>
</template>

<script>
  export default {
      data: () => ({
          name: '',
          model: '',
          aviailability: null,
          state: null
      }),
      methods: {
          reset(){
              this.name = '',
              this.model = '',
              this.aviailability = null,
              this.state = null
          },
          add(){
              this.$emit('add', {
                  name : this.name,
                  model : this.model,
                  aviailability : this.aviailability,
                  state : this.state
              });
              this.reset()
          }
      }
  }
</script>

<style scoped>
    .margin-bottom{
      margin-bottom: 12px;
    }
</style>