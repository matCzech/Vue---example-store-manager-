<template>
    <div class="col-md-6">
        <div class="panel panel-primary">
          <div class="panel panel-heading">
            <div class="panel-title" style="display:flex;justify-content:space-between;">
              <h4>Multimetr</h4>
              <button type="button" class="btn btn-danger" @click="remove">Usuń</button>
            </div>
          </div>
          <div class="panel panel-body">
            <div class="input-group">
                  <span class="input-group-addon margin-bottom">Nazwa</span>
                  <input type="text" v-model="name" class="form-control" placeholder="Nazwa">
            </div>
            <div class="input-group">
                  <span class="input-group-addon margin-bottom">Model</span>
                  <input type="text" v-model="model" class="form-control" placeholder="Model">
          </div>            
        </div>
      </div>
    </div>
</template>

<script>
  export default {
      data: () => ({

      })
  }
</script>

<style scoped>
    .margin-bottom{
      margin-bottom: 12px;
    }
</style>