<template>
    <div
        class="px-8 py-20 md:px-12 lg:px-10 flex items-center justify-center backdrop-blur-3xl !bg-cover !bg-center !bg-no-repeat"
        style="background-image: url('https://www.wallpaperflare.com/static/930/175/684/circles-highlights-background-form-wallpaper-preview.jpg'); object-fit: cover;"
    >
        <div class="px-8 md:px-12 lg:px-20 py-12 flex flex-col items-center gap-12 w-full max-w-xl backdrop-blur-2xl rounded-2xl bg-white/10 border border-white/10">
            <div class="flex flex-col items-center gap-4 w-full">
                <i class="pi pi-spin pi-globe text-white" style="font-size: 3rem"></i>
                <div class="flex flex-col gap-2 w-full">
                    <div class="text-center text-3xl font-medium text-white leading-tight">Welcome Back</div>
                </div>
            </div>
            <div class="flex flex-col items-center gap-8 w-full">
                <div class="flex flex-col gap-6 w-full">
                    <IconField>
                        <InputIcon class="pi pi-user !text-white/70" />
                        <InputText type="text" class="!appearance-none !border !border-white/10 !w-full !outline-0 !bg-white/10 !text-white placeholder:!text-white/70 !rounded-3xl !shadow-sm" placeholder="Username" value="example@example.com" />
                    </IconField>
                    <IconField>
                        <InputIcon class="pi pi-lock !text-white/70" />
                        <InputText
                            type="password"
                            class="!appearance-none !border !border-white/10 !w-full !outline-0 !bg-white/10 !text-white placeholder:!text-white/70 !rounded-3xl !shadow-sm"
                            placeholder="Password"
                            value="123456"
                        />
                    </IconField>
                </div>
                <Button label="Sign In" class="!w-full !rounded-3xl !bg-surface-950 !border !border-surface-950 !text-white hover:!bg-surface-950/80" @click="gotToHome" />
            </div>
            <a class="text-white/80 cursor-pointer hover:text-white/90">Forgot Password?</a>
        </div>
    </div>
</template>
<script setup>
import Button from 'primevue/button';
import IconField from 'primevue/iconfield';
import InputIcon from 'primevue/inputicon';
import InputText from 'primevue/inputtext';
import { useRouter } from 'vue-router';
const router = useRouter();

const gotToHome = () => {
  router.push({ name: 'home' });
}
</script>
