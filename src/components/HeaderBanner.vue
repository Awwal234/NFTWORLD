<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    data() {
        return {
            home: 'Home',
            market: 'Marketplace',
            activity: 'Activity',
            community: 'Community',
        }
    }
})
</script>

<template>
    <div class="py-[46.5px] px-[80px] flex items-center justify-between">
        <div class="font-[700] text-[32px] text-[#EA6B00] leading-[43.2px]">
            NFTS<span class="text-[24px] leading-[32.4px] text-[#3F3F3F]">world</span>
        </div>
        <div class="lg:space-x-[30px] xlg:space-x-[80px] flex font-[500] lg:text-[17px] xlg:text-[24px] leading-[32.4px]">
            <div class="text-[#EA6B00] cursor-pointer">{{ home }}</div>
            <div class="cursor-pointer">{{ market }}</div>
            <div class="cursor-pointer">{{ activity }}</div>
            <div class="cursor-pointer">{{ community }}</div>
        </div>
        <!--buttton-->
        <div
            class="rounded-[8px] text-[#fff] lg:text-[17px] xlg:text-[24px] font-[500] leading-[32.4px] font-[#fff] bg-[#EA6B00] px-[45.5px] py-[10px] text-center cursor-pointer">
            Sign up
        </div>
        <!---->
    </div>
</template>

<style></style>