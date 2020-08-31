<template>
    <v-main>
        <v-row>
            <v-col cols="12"><h1>Bartender App</h1></v-col>
        </v-row>
        <v-row class="ma-0 pa-0">
            <v-col cols="4"></v-col>
            <v-col cols="6">
                <v-radio-group v-model="selected" row>
                    <v-radio label="Bartender Menu" name="selection" value="BartenderMenu"></v-radio>
                    <v-radio label="Customer Menu" name="selection" value="CustomerMenu"></v-radio>
                </v-radio-group>
            </v-col>
        </v-row>
        <BartenderMenu v-if="selected==='BartenderMenu'"/>
        <CustomerMenu v-if="selected==='CustomerMenu'"/>
    </v-main>
</template>
<script>
    import BartenderMenu from "@/components/BartenderMenu";
    import CustomerMenu from "@/components/CustomerMenu";
    export default {
        name: "Home",
        components:{
            BartenderMenu,
            CustomerMenu
        },
        data() {
            return {
                selected: 'CustomerMenu'
            }
        }

    }
</script>