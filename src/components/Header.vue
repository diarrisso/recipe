<template>
    <div>
        <header>
          <input placeholder="suche..."/>
        </header>
    </div>
</template>

<script>
    export default {
        name: 'Header'
        
    }
</script>


<style scoped>

  body {
    margin: 0;
    
  }
 
  header {

    background-color: aqua;
    height: 120px;
    padding: 16px;
    display: flex;
    align-items: flex-end;
    border-bottom-right-radius: 8px;
    border-bottom-left-radius: 8px;
  }


  input {

    border: 0;
    border-radius:  8px;
    width: 100%;
    height: 30px;
  }


</style>


