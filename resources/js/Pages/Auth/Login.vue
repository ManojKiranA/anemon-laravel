<template>
    <Head title="Log in"/>

    <t-login
        :canResetPassword="canResetPassword"
        :radius="5"
        :status="status"
        bg-image="/img/samples/bgFakurianDesign-nY14Fs8pxT8-unsplash-compressed.jpg"
        login-button-color="purple"
        register-button-design="link-plus"
        register-button-color="purple"
        color="solid-purple"
    >
        <!--Logo-->
        <template #logo>
            <Link href="/">
                <div class="flex flex-col space-x-2 items-center max-w-min py-2">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z" />
                    </svg>
                    <span class="text-5xl mt-1">Anemon</span>
                </div>
            </Link>
        </template>
        <!--Greeting-->
        <template #greeting>
            Sign in to your account
        </template>
    </t-login>
</template>

<script>
import {defineComponent} from 'vue'
import TLogin from "@/Components/Auth/TLogin";
import TLogo from "@/Components/Icon/TLogo";
import {Head, Link} from '@inertiajs/inertia-vue3';

export default defineComponent({
    components: {
        Head,
        TLogo,
        TLogin,
        Link
    },

    props: {
        canResetPassword: Boolean,
        status: String
    }
})
</script>
