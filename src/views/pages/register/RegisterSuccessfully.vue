<script setup>
import { ref } from 'vue';

import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap-vue/dist/bootstrap-vue.css';

const imageLink = ref('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT0CorRpYgS6tIGKcL1dvEriV8s26petffgShzIK0Zl5g&s');


</script>


<template>
    <div class="registration-container row login-container">
        <img class="col-4 view-height" :src="imageLink" alt="ảnh">
        <form @submit.prevent="handleRegistration" class="col-8 view-height">
            <div class="parent_register_container col-12 md:col-6">
                <div class="p-fluid register-input-container">
                    <h1>Congratulations! Your registration was successful.</h1>
                    <p>Congratulations! Your registration was successful.</p>
                    <p>Please check your email and verify your account to unlock the full potential of job opportunities. Best of luck on your career journey!</p>
                    <Button label="Register" severity="register" class="mb-2 mr-2" />
                </div>
            </div>
        </form>
    </div>
</template>

<style scoped>
.login-container {
    height: 100vh;
}


.parent_register_container {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}

.register-input-container {
    width: 650px;
    height: 400px;
}

.view-height {
    height: 100%;
}

.display_vertical {
    display: flex;
    flex-direction: row;
}

.display_horizontal {
    display: flex;
    flex-direction: row;
}

.item_space_between {
    justify-content: space-between;
}

.self_center {
    text-align: center;
}
</style>