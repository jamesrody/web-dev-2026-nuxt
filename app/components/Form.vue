<template>
    <div>
        <UForm @submit="processForm" class="text-center max-w-40 mx-auto">
            <UFormField label="First Name">
                <UInput v-model="firstName"></UInput>
            </UFormField>
            <UFormField label="Last Name">
                <UInput v-model="lastName"></UInput>
            </UFormField>
            <UFormField label= "Email">
                <UInput v-model="email"></UInput>
            </UFormField>
            <UButton type="submit" class="mt-4">
                Submit
            </UButton>
        </UForm>
        <div v-if="submitted==true">
            Hi, my first name is {{ submittedFirstName }} {{ submittedLastName }}, and my email is {{ submittedEmail }}
        </div>
    </div>
</template>


<script setup>

const firstName = ref('')
const submittedFirstName = ref('')
const lastName = ref('')
const submittedLastName = ref('')
const email = ref('')
const submittedEmail = ref('')
const submitted = ref(false)
function processForm(event){
    submittedFirstName.value = firstName.value
    submitted.value = true;
    firstName.value = ""
    submittedLastName.value = lastName.value
    submitted.value = true;
    lastName.value = ""
    submittedEmail.value = email.value
    submitted.value = true;
    email.value = ""
    alert(`Hi ${submittedFirstName.value} ${submittedLastName.value}`)
}

</script>