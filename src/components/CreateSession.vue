<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    data() {
        return {
            creates: [
                {
                    'img': '/img/okay.svg',
                    'content': 'connect your wallet'
                },
                {
                    'img': '/img/okayy.svg',
                    'content': 'Create your collections'
                },
                {
                    'img': '/img/okayyy.svg',
                    'content': 'Sell your NFTs'
                },
            ] as any
        }
    }
})
</script>

<template>
    <div class="mt-[80px] px-[80px]">
        <div class="mx-auto text-[#3F3F3F] text-center font-[700] text-[48px] leading-[64.8px]">
            Create & sell your NFTs
        </div>
        <!---->
        <div class="mt-[40px] w-full">
            <div class="w-fit mx-auto flex space-x-[30px]">
                <!---->
                <div v-for="create in creates" :key="create"
                    class="w-fit justify-center py-[64px] border border-[#D6D6D6] px-[32px]">
                    <div class="w-fit mx-auto"><img :src="create.img" class="mx-auto" alt="" /></div>
                    <div class="mt-[16px] mx-auto text-center text-[#3F3F3F] font-[700] text-[40px] leading-[54px]">
                        {{ create.content }}
                    </div>
                </div>
                <!---->
            </div>
            <!---->
            <div>
                <div
                    class="rounded-[8px] mt-[30px] w-fit mx-auto text-[#fff] lg:text-[17px] xlg:text-[24px] font-[400] leading-[32.4px] font-[#fff] bg-[#EA6B00] px-[46.5px] py-[12px] text-center cursor-pointer">
                    Get started
                </div>
            </div>
            <!---->
        </div>
        <!---->
    </div>
</template>

<style scoped></style>