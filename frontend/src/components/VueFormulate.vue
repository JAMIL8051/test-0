<template>
    <div>
        <h2>Vue Formulate</h2>
        <FormulateForm v-model="formValues" @submit="handleSubmit">
            <FormulateInput name ="name" label="Name" validation="required"/>
            <FormulateInput type ="email" label="Email" validation="required|email"/>
            <FormulateInput type ="submit" label="Sign Up" />
        </FormulateForm>
        <h3>Vaues:</h3>
        {{formValues}}

    </div>
</template>

<script>
export default {
    data: () => ({
    formValues: {}
    }),
    methods:{
        handleSubmit(){
            console.log(this.formValues)

        }
    } 
};
</script>