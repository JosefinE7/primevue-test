<template>
    <form>
        <div class="p-fluid p-formgrid p-grid">
            <div class="p-field p-col-6">
                <label for="fullname">Full name</label>
                <InputText id="fullname" type="text" placeholder="Full name"/>
            </div>
            <div class="p-field p-col-6">
                <label for="owner">Owner</label>
                <InputText id="owner" type="text" placeholder="Owner"/>
            </div>
            <div class="p-field p-col-6">
                <label for="lastname">Lastname2</label>
                <InputText id="lastname" type="text" />
            </div>
            <div class="p-field p-col-6">
                <label for="lastname">Lastname3</label>
                <InputText id="lastname" type="text" />
            </div>
            <div class="p-field p-col-6">
                <label for="network">Network Functions</label>
                <Dropdown inputId="network" v-model="selectedNetwork" :options="networks" optionLabel="name" placeholder="Select network functions" />
            </div>
            <div class="p-col-6">
                
            </div>
            <div class="p-field p-col-6">
                <label for="placement">Placement</label>
                <Dropdown inputId="placement" v-model="selectedPlacement" :options="placements" optionLabel="name" placeholder="Placement" />
            </div>
            <div class="p-col-6">
                
            </div>
            <div class="p-col-12">
                <label for="lastname">Lastname6</label>
                <InputText id="lastname" type="text" />
            </div>
            <div class="p-col-12">
                <label for="lastname">Address</label>
                <InputText id="lastname" rows="4" type="text"/>
            </div>
        </div>
        <Button label="Submit" icon="pi pi-check" iconPos="left" />
    </form>
</template>

<script>

export default {
    data() {
        return {
            selectedNetowrk: null,
            networks: [
                {name: 'New York', code: 'NY'},
                {name: 'Rome', code: 'RM'},
                {name: 'London', code: 'LDN'},
                {name: 'Istanbul', code: 'IST'},
                {name: 'Paris', code: 'PRS'}
            ],
            selectedPlacement: null,
            placements: [
                {name: 'New York', code: 'NY'},
                {name: 'Rome', code: 'RM'},
                {name: 'London', code: 'LDN'},
                {name: 'Istanbul', code: 'IST'},
                {name: 'Paris', code: 'PRS'}
            ]
        }
    }
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