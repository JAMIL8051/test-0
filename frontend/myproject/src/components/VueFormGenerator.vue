<template>
  <div>
    <h2>Vue Form Generator</h2>
    <vue-form-generator
      :schema="schema"
      :model="model"
      :options="formOptions"
    ></vue-form-generator>
    <h3>Values</h3>
    {{model}}

  </div>
</template>

<script>
export default {
    data: () => ({
        model: {
            name: '',
            email: ''

        },
        schema: {
            fields [
                {
                    type: 'input',
                    inputType: 'text',
                    label: 'Name',
                    model: 'name',
                    required: true,
                    validator: 'string'
                },
                {
                    type: 'input',
                    inputType: 'email',
                    label: 'Email',
                    model: 'email',
                    required: true,
                    placeholder: 'email@test.com',
                    validator: 'email'
                },
                {
                    type: 'input',
                    inputType: 'text',
                    label: 'Member',
                    model: 'member',
                    required: true,
                    validator: 'string'
                    
                },
                {
                    type: 'submit',
                    onSubmit(model){
                        console.log(model)

                    },
                    label: '',
                    buttonText: 'Sign Up',
                    validateBeforeSubmit: true
                }
            ]
        },
        formOptions: {
            validateAfterLoad: false,
            validateAfterChange: true,
            validateAsync: true
        }

    })
};
</script>