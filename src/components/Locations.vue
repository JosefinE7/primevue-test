<template>
    <form @submit.prevent="handleSubmit(!v$.$invalid)">
        <div class="p-fluid p-formgrid p-grid">
            <!-- Full name field -->
            <div class="p-field p-col-6">
                <label for="fullname">Full name</label>
                <InputText id="fullname" type="text" placeholder="Full name" required/>
            </div>
            <!-- Owner field -->
            <div class="p-field p-col-6">
                <label for="owner">Owner</label>
                <InputText id="owner" type="text" placeholder="Owner" required/>
            </div>
            <!-- Status field -->
            <div class="p-field p-col-6">
                <label for="state">Status</label>
                <CascadeSelect v-model="selectedState" :options="status" optionLabel="cname" optionGroupLabel="name" 
                        :optionGroupChildren="['substatus']" style="minWidth: 14rem" placeholder="Status" required/>
            </div>
            <!-- Substatus field -->
            <div class="p-field p-col-6">
                
            </div>
            <!-- Network functions field -->
            <div class="p-field p-col-6">
                <label for="network">Network Functions</label>
                <Dropdown inputId="network" v-model="selectedNetwork" :options="networks" optionLabel="name" 
                        placeholder="Select network functions" />
            </div>
            <!-- Empty field -->
            <div class="p-col-6">
                
            </div>
            <!-- Placement field -->
            <div class="p-field p-col-6">
                <label for="placement">Placement</label>
                <Dropdown inputId="placement" v-model="selectedPlacement" :options="placements" optionLabel="name" 
                        placeholder="Placement" required/>
            </div>
            <!-- Empty field -->
            <div class="p-col-6">
                
            </div>
            <!-- Aliases field -->
            <div class="p-field p-col-12"> 
                <label for="aliase">Aliases</label>
                <Dropdown inputId="aliase" v-model="selectedAliase" :options="aliases" optionLabel="name" 
                        placeholder="Aliases" editable required />
            </div>
            <!-- Directions field -->
            <div class="p-col-12">
                <label for="directions">Directions</label>
                <Textarea inputId="directions" v-model="value" :autoResize="true" rows="5" cols="30" required />
            </div>
        </div>
        <!-- Submit button -->
        <div class="p-d-flex p-jc-end">
            <Button label="Create" type="submit" icon="pi pi-check" iconPos="left" @click="submit" />
            <Toast />
        </div>
    </form>
</template>

<script>


export default {
    data() {
        return {
            // Status and substatus data
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
            // Network functions data
            selectedNetwork: null,
            networks: [
                {name: 'Switching: BNG, CG-NAT, routers'},
                {name: 'Tunnelling gateway elements: IPSec/SSL VPN gateways'},
                {name: 'Traffic analysis: DPI, QoE measurementI'},
                {name: 'Signalling: SBCs, IMS'}
            ],
            // Placement data
            selectedPlacement: null,
            placements: [
                {name: 'Stockholm'},
                {name: 'Göteborg'},
                {name: 'Malmö'},
                {name: 'Kiruna'}
            ],
            // Aliases data
            selectedAliase: null,
            aliases: [
                {name: 'AA77'},
                {name: 'AB35'},
                {name: 'CB56'},
                {name: 'LL89'},
                {name: 'TT78'}
            ]
        }
    },
    // Success toast method
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
        background-color: #0e2f44;
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
        padding: 10px 6px;
        width: 100%;
        box-sizing: border-box;
        border: 1px solid #52527a;
        border-radius: 2px;
        font-size: 1em;
    }

</style>