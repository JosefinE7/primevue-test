<template>
    <form>
        <div class="p-grid">
            <div class="p-col-6">
                <label for="firstname">Firstname</label>
                <InputText id="firstname" type="text" />
            </div>
            <div class="p-col-6">
                <label for="lastname">Lastname</label>
                <InputText id="lastname" type="text" />
            </div>
            <div class="p-col-6">6</div>
            <div class="p-col-6">6</div>
        </div>
    </form>
</template>

<script>

export default {

}
</script>

<style>
    form {
        max-width: 720px;
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
        font-size: 1.2em;
        letter-spacing: 1px;
        
    }
    input {
        /* display: block; */
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