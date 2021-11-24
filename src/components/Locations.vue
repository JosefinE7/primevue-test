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
                <label for="state">Status</label>
                <CascadeSelect v-model="selectedCity" :options="countries" optionLabel="cname" optionGroupLabel="name" 
                        :optionGroupChildren="['states', 'cities']" style="minWidth: 14rem" />
            </div>
            <div class="p-field p-col-6">
                
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
            <div class="p-field p-col-12"> 
                <label for="aliase">Aliases</label>
                <Dropdown inputId="aliase" v-model="selectedAliase" :options="aliases" optionLabel="name" placeholder="Aliases" editable />
            </div>
            <div class="p-col-12">
                <label for="directions">Directions</label>
                <Textarea inputId="directions" v-model="value" :autoResize="true" rows="5" cols="30" />
            </div>
        </div>
        <Button label="Submit" icon="pi pi-check" iconPos="left" />
    </form>
</template>

<script>
export default {
    data() {
        return {
            selectedCity: null,
            countries: [
                {
                    name: 'Australia',
                    code: 'AU',
                    states: [
                        {
                            name: 'New South Wales',
                            cities: [
                                {cname: 'Sydney', code: 'A-SY'},
                                {cname: 'Newcastle', code: 'A-NE'},
                                {cname: 'Wollongong', code: 'A-WO'}
                            ]
                        },
                        {
                            name: 'Queensland',
                            cities: [
                                {cname: 'Brisbane', code: 'A-BR'},
                                {cname: 'Townsville', code: 'A-TO'}
                            ]
                        },
                        
                    ]
                },
                {
                    name: 'Canada', 
                    code: 'CA',
                    states: [
                        {
                            name: 'Quebec',
                            cities: [
                                {cname: 'Montreal', code: 'C-MO'},
                                {cname: 'Quebec City', code: 'C-QU'}
                            ]
                        },
                        {
                            name: 'Ontario',
                            cities: [
                                {cname: 'Ottawa', code: 'C-OT'},
                                {cname: 'Toronto', code: 'C-TO'}
                            ]
                        },
                        
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