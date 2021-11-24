<template>
    <form @submit.prevent="handleSubmit(!v$.$invalid)">
        <div class="p-fluid p-formgrid p-grid">
            <div class="p-field p-col-6">
                <label for="fullname">Full name</label>
                <InputText id="fullname" type="text" placeholder="Full name" required/>
            </div>
            <div class="p-field p-col-6">
                <label for="owner">Owner</label>
                <InputText id="owner" type="text" placeholder="Owner" required/>
            </div>
            <div class="p-field p-col-6">
                <label for="state">Status</label>
                <CascadeSelect v-model="selectedState" :options="status" optionLabel="cname" optionGroupLabel="name" 
                        :optionGroupChildren="['substatus']" style="minWidth: 14rem" placeholder="Status" required/>
            </div>
            <div class="p-field p-col-6">
                
            </div>
            <div class="p-field p-col-6">
                <label for="network">Network Functions</label>
                <Dropdown inputId="network" v-model="selectedNetwork" :options="networks" optionLabel="name" 
                        placeholder="Select network functions" />
            </div>
            <div class="p-col-6">
                
            </div>
            <div class="p-field p-col-6">
                <label for="placement">Placement</label>
                <Dropdown inputId="placement" v-model="selectedPlacement" :options="placements" optionLabel="name" 
                        placeholder="Placement" required/>
            </div>
            <div class="p-col-6">
                
            </div>
            <div class="p-field p-col-12"> 
                <label for="aliase">Aliases</label>
                <Dropdown inputId="aliase" v-model="selectedAliase" :options="aliases" optionLabel="name" 
                        placeholder="Aliases" editable required />
            </div>
            <div class="p-col-12">
                <label for="directions">Directions</label>
                <Textarea inputId="directions" v-model="value" :autoResize="true" rows="5" cols="30" required />
            </div>
        </div>
        <Button label="Submit" type="submit" icon="pi pi-check" iconPos="left" @click="submit" />
        <Toast />
    </form>
</template>

<script>


export default {
    data() {
        return {
            selectedState: null,
            status: [
                {
                    name: 'Constructed',
                    substatus: [
                        {cname: 'Constructed'},
                        {cname: 'Frozen'},
                        {cname: 'Planned for Termination'},
                        {cname: 'Termination Ordered'}
                    ]
                },
                {
                    name: 'Initiated',
                    substatus: [
                        {cname: 'Initiated'},
                        {cname: 'Accepted'},
                        {cname: 'Rejected'},
                        {cname: 'Cancelled'}
                    ]
                },
            ],
            selectedNetwork: null,
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
            ],
            selectedAliase: null,
            aliases: [
                {name: 'New York', code: 'NY'},
                {name: 'Rome', code: 'RM'},
                {name: 'London', code: 'LDN'},
                {name: 'Istanbul', code: 'IST'},
                {name: 'Paris', code: 'PRS'}
            ]
        }
    },
    methods: {
        submit() {
            this.$toast.add({severity: 'success', summary: 'Location successfully created'});
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