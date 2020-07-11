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
            <div class="col-md-6">
              <div class="input-group margin-bottom">
                    <span class="input-group-addon"><em>Marka</em></span>
                    <span class="input-group-addon"><b>{{name}}</b></span>
              </div>
              <div class="input-group margin-bottom">
                    <span class="input-group-addon"><em>Model</em></span>
                    <span class="input-group-addon"><b>{{model}}</b></span>
              </div>  
          </div> 
          <div class="margin-bottom row">
            <div class="col-md-6">
                <div class="progress">
                    <div class="progress-bar progress-bar-danger progress-bar-striped" role="progress-bar" style="width: 100%;">
                      <b>{{aviailability}}</b>{{aviailability}}
                    </div>
                </div>
            </div>  
            <div class="col-md-6">
                <div class="progress">
                    <div class="progress-bar progress-bar-primary progress-bar-striped" role="progress-bar" style="width: 100%;">
                      <b>{{state}}</b>{{state}}
                    </div>
                </div>
            </div>  
          </div>      
        </div>
      </div>
    </div>
</template>

<script>
  export default {
      props: {
          name: String,
          model: String,
          aviailability: Number,
          state: Number
      },
      methods: {
          remove(){
            this.$emit('remove', this.name);
          }
      }

  }
</script>

<style scoped>
    .margin-bottom{
      margin-bottom: 12px;
    }
</style>