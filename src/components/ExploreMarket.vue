<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    data() {
        return {
            creates: [
                {
                    'img': '/img/nfts.png',
                    'content': '8h:53m:20s',
                    'biding': '1000 eth'
                },
                {
                    'img': '/img/nftss.png',
                    'content': '10h:53m:20s',
                    'biding': '2400 eth'
                },
                {
                    'img': '/img/nftsss.png',
                    'content': '11h:53m:20s',
                    'biding': '1500 eth'
                },
                {
                    'img': '/img/nftssss.png',
                    'content': '11h:20m:20s',
                    'biding': '250 eth'
                },
            ] as any,
            latest: 'Latest NFTs',
            building: 'Building',
            music: 'Music',
            vw: 'Virtual world',
            sculpture: 'Sculpture',
            tc: 'Trading cord'
        }
    }
})
</script>

<template>
    <div class="mt-[80px] px-[80px]">
        <div class="mx-auto text-[#3F3F3F] text-center font-[700] text-[48px] leading-[64.8px]">
            Explore Marketplace
        </div>
        <div class="mt-[36px] mx-auto">
            <div
                class="lg:space-x-[30px] justify-center text-[#3F3F3F] xlg:space-x-[65px] flex items-center font-[500] lg:text-[17px] xlg:text-[24px] leading-[32.4px]">
                <div class="text-[#fff] rounded-[8px] px-[16px] py-[10px] bg-[#EA6B00] cursor-pointer">{{ latest }}</div>
                <div class="cursor-pointer">{{ building }}</div>
                <div class="cursor-pointer">{{ music }}</div>
                <div class="cursor-pointer">{{ vw }}</div>
                <div class="cursor-pointer">{{ sculpture }}</div>
                <div class="cursor-pointer">{{ tc }}</div>
            </div>
        </div>
        <!---->
        <div class="mt-[40px] create_board overflow-x-scroll w-full">
            <div class="mt-[40px] flex mx-auto w-fit space-x-[20px]">
                <div v-for="create in creates" :key="create" class="w-[388px]">
                    <!---->
                    <div class="">
                        <div class="rounded-[8px] border border-[#D6D6D6] w-full">
                            <img :src="create.img" class="rounded-t-[8px]" />
                            <div class="mt-[32px] px-[16px] pb-[32px]">
                                <div>
                                    <div
                                        class="flex font-[400] text-[#3F3F3F] mt-[32px] leading-[32.4px] text-[24px] justify-between">
                                        <div>Remaining time</div>
                                        <div>{{ create.content }}</div>
                                    </div>
                                    <div class="flex text-[#3F3F3F] font-[400] mt-[4px] leading-[32.4px] justify-between">
                                        <div class="text-[24px] text-[#3F3F3F]">Current bid</div>
                                        <div class="text-[32px] font-[500] text-[#DE5A10]">{{ create.biding }}</div>
                                    </div>
                                </div>
                                <!---->
                                <div>
                                    <div
                                        class="rounded-[8px] mt-[30px] w-fit mx-auto text-[#fff] lg:text-[17px] xlg:text-[24px] font-[400] leading-[32.4px] font-[#fff] bg-[#EA6B00] px-[57.5px] py-[12px] text-center cursor-pointer">
                                        Place bid
                                    </div>
                                </div>
                                <!---->
                            </div>
                        </div>
                    </div>
                    <!---->
                </div>
            </div>
        </div>
        <!---->
        <div>
            <div
                class="rounded-[8px] font-[600] mt-[30px] w-fit mx-auto text-[#DE5A10] lg:text-[17px] xlg:text-[24px] font-[400] leading-[43.2px] text-center cursor-pointer">
                View more
            </div>
        </div>
        <!---->
    </div>
</template>

<style scoped>
.create_board::-webkit-scrollbar {
    display: none;
}
</style>