<script setup>
import { ref } from 'vue';

import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap-vue/dist/bootstrap-vue.css';

const imageLink = ref('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT0CorRpYgS6tIGKcL1dvEriV8s26petffgShzIK0Zl5g&s');

const registrationForm = ref({
    name: '',
    email: '',
    password: ''
});

const handleRegistration = () => {
    // Xử lý đăng ký ở đây
    console.log('Đăng ký với:', registrationForm.value);
};

</script>


<template>
    <div class="registration-container row login-container">
        <img class="col-4 view-height" :src="imageLink" alt="ảnh">
        <form @submit.prevent="handleRegistration" class="col-8 view-height">
            <div class="parent_register_container col-12 md:col-6">
                <div class="p-fluid register-input-container">
                    <h2>Register with us</h2>
                    <h1>Explore open career opportunities</h1>
                    <div class="field">
                        <label for="email">Email</label>
                        <InputText id="email" type="text" />
                    </div>
                    <div class="field">
                        <label for="password">Password</label>
                        <InputText id="email" type="password" />
                    </div>
                    <div class="field">
                        <label for="phon-number">Phone number</label>
                        <InputText id="phon-number" type="text" />
                    </div>
                    <div class="row">
                        <div class="col-6">
                            <p class="">X 8 characters minimum</p>
                            <p class="">X 1 number</p>
                        </div>
                        <div class="col-6">
                            <p>X 1 specical characters</p>
                            <p>X 1 uppercase characters</p>
                        </div>
                    </div>
                    <Button label="Register" severity="register" class="mb-2 mr-2" />

                    <div class="self_center mt-3">
                        <p>Already have an acount? <a href="#">Login</a></p>
                    </div>
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
    width: 650;
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