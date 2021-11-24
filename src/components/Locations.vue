<template>
  <form>
      <label>Email:</label>
      <input type="email" required>
  </form>
</template>

<script>
export default {

}
</script>

<style>
    form {
        max-width: 420px;
        margin: 30px auto;
        background-color: #33334d;
        text-align: left;
        padding: 40px;
        border-radius: 10px;
    }
    label {
        color: #ffe;
        display: inline-block;
        margin-bottom: 5px;
        font-size: 1em;
        letter-spacing: 1px;
        
    }
    input {
        display: block;
        padding: 10px 6px;
        width: 100%;
        box-sizing: border-box;
        border: 1px solid #52527a;
        border-radius: 2px;
        font-size: 1em;
        color:#fff;
        background-color: #29293d;
    }

</style>