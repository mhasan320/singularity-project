<template>
<div class="amazingNft">
    <div class="nft-left">
        <h3>The amazing NFT art of the world here</h3>
    </div>
    <div class="nft-right">
        <div class="single-nft">
            <IconFast/>
            <div class="nfttext">
                <h4>Fast Transaction</h4>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam etiam viverra tellus imperdiet.</p>
            </div>
        </div>
        <div class="single-nft">
            <IconGrouth/>
            <div class="nfttext">
                <h4>Growth Transaction</h4>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam etiam viverra tellus</p>
            </div>
        </div>
    </div>
</div>
</template>

<script setup>
    import IconFast from './icons/IconFast.vue';
    import IconGrouth from './icons/IconGrouth.vue';
</script>

<style scoped lang="scss">
    .amazingNft{
        padding: 5rem 5rem;
        gap: 60px;
        display: flex;
        justify-content: space-between;
        background: rgba(217, 224, 236, 0.2);
        backdrop-filter: blur(25px);
    }
    .nft-left{
        width: 35%;
    }
    .nft-left h3{
        font-family: 'integral_cfmedium';
        font-style: normal;
        font-weight: 700;
        color:#000;
        font-size: 28px;
        line-height: 34px;
    }
    .nft-right{
        display: flex;
        width: 75%;
        gap: 30px;
        justify-content: space-between;
    }
    .single-nft{
        display: flex;
        justify-content: start;
        gap: 20px;
    }
    .nfttext h4{
        font-style: normal;
        font-weight: 700;
        font-size: 20px;
        line-height: 26px;
        margin-bottom: 10px;
    }
    .nfttext p{
        font-style: normal;
        font-weight: 400;
        font-size: 14px;
        line-height: 160%;
    }
</style>