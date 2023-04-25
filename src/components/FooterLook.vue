<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    data() {
        return {
            year: 0 as number,
        }
    },
    methods: {
        getYear: function () {
            const date = new Date();
            const year = date.getFullYear();
            this.year = year;
        },
    },
    mounted() {
        this.getYear()
    }
});
</script>

<template>
    <div class="py-[48px] px-[80px] mt-[40px] flex items-center justify-between">
        <div class="font-[700] text-[32px] text-[#EA6B00] leading-[43.2px]">
            NFTS<span class="text-[24px] leading-[32.4px] text-[#3F3F3F]">world</span>
        </div>
        <div class="font-[700] text-[17px] leading-[32.4px] text-[#3F3F3F]">
            &copy; {{ year }} NFTs world. All rights reserved
        </div>
        <div class="flex items-center space-x-[30px]">
            <div class="cursor-pointer"><img src="/img/twitterdark.svg" class="" alt="" /></div>
            <div class="cursor-pointer"><img src="/img/discorddark.svg" class="" alt="" /></div>
        </div>
    </div>
</template>