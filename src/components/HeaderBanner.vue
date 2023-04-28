<script lang="ts">
import { defineComponent } from 'vue'
import SignForm from './SignForm.vue';

export default defineComponent({
    components: {
        SignForm,
    },
    data() {
        return {
            home: 'Home' as string,
            market: 'Marketplace' as string,
            activity: 'Activity' as string,
            community: 'Community' as string,
            menu: false as boolean,
        }
    },
    methods: {
        openMenu() {
            this.menu = true;
        },
        closeMenu() {
            this.menu = false;
        }
    }
})
</script>

<template>
    <div>
        <div class="py-[46.5px] px-[80px] flex items-center justify-between">
            <div class="font-[700] text-[32px] text-[#EA6B00] leading-[43.2px]">
                NFTS<span class="text-[24px] leading-[32.4px] text-[#3F3F3F]">world</span>
            </div>
            <div
                class="lg:space-x-[30px] xlg:space-x-[80px] flex font-[500] lg:text-[17px] xlg:text-[24px] leading-[32.4px]">
                <div class="text-[#EA6B00] cursor-pointer">{{ home }}</div>
                <div class="cursor-pointer">{{ market }}</div>
                <div class="cursor-pointer">{{ activity }}</div>
                <div class="cursor-pointer">{{ community }}</div>
            </div>
            <!--buttton-->
            <div @click='openMenu'
                class="rounded-[8px] text-[#fff] lg:text-[17px] xlg:text-[24px] font-[500] leading-[32.4px] font-[#fff] bg-[#EA6B00] px-[45.5px] py-[10px] text-center cursor-pointer">
                Sign up
            </div>
            <!---->
        </div>
        <!---->
        <div v-show="menu" class="fixed w-full pb-[50px] overflow-y-scroll left-0 top-0 h-full menu_wrap">
            <div
                class="mt-[108px] pt-[24px] rounded-[8px] h-fit mx-auto md:w-[600px] bg-[#fff] lg:w-[800px] xlg:w-[1038px]">
                <!--head tab-->
                <div class="flex items-center px-[96px] mx-auto">
                    <div
                        class="px-[53px] cursor-pointer rounded-[8px] bg-[#DE5A10] font-[700] text-[#fff] leading-[27px] text-[20px] py-[10.5px]">
                        Wallet Sign up
                    </div>
                    <div
                        class="px-[53px] cursor-pointer ml-[24px] rounded-[8px] bg-[transparent] font-[700] text-[#3F3F3F] leading-[27px] text-[20px] py-[10.5px]">
                        Email Sign up
                    </div>
                    <div class="ml-[80px]">
                        <img @click='closeMenu' src="/img/X.svg" class="cursor-pointer" />
                    </div>
                </div>
                <!--close head tab-->
                <SignForm />
                <!--contents-->
            </div>
        </div>
        <!---->
    </div>
</template>

<style>
.menu_wrap {
    background: rgba(209, 207, 207, 0.5);
}

.menu_wrap::-webkit-scrollbar {
    display: none;
}
</style>