<template>
<div class="landing-section">
    <div class="landing-left">
        <h3>Discover, and collect Digital Art  NFTs </h3>
        <p>Digital marketplace for crypto collectibles and non-fungible tokens (NFTs). Buy, Sell, and discover exclusive digital assets.</p>
        <button class="explore">Explore Now</button>
        <ul>
            <li>
                <span>98K + </span>
                Artwork
            </li>
            <li>
                <span>12K + </span>
                Auction
            </li>
            <li>
                <span>15K + </span>
                Artist
            </li>
        </ul>
        <img src="../assets/dotbg.png" alt="dot bg"/>
    </div>
    <div class="landing-right">
        <div class="crbtw">
            <h3>Abstr Gradient NFT</h3>
            <div class="user">
                <img src="../assets/user.png" alt="user">
                <span>Arkhan17</span>
            </div>
        </div>
        <div class="currentBit">
            <div class="bit2">
                <h3>Current Bit</h3>
                <span class="flexbit">
                    <img src="../assets/ethuram.png" alt="ethuram">
                    0.25 ETH
                </span>
            </div>
            <div class="bit2">
                <h3>Ends in</h3>
                <span>12h  43m  42s</span>
            </div>
        </div>
        <div class="abosolutePosition">
            <img src="../assets/absolute.png" alt="absolute"/>
        </div>
        <img src="../assets/bg2.png" alt="bg" class="bg2"/>
        <img src="../assets/bg3.png" alt="bg" class="bg3"/>
    </div>
</div>
</template>

<style scoped lang="scss">
    .landing-section{
        padding: 6rem 5rem;
        gap: 20px;
        display: flex;
        justify-content: space-between;
    }
    .landing-left{
        width: 45%;
        position: relative;
    }
    .landing-left h3{
        font-size: 40px;
        color: #000;
        line-height: 1.1;
        padding-bottom: 8px;
        font-family: 'integral_cfmedium';
        text-transform: uppercase;
    }
    .landing-left p{
        font-size: 20px;
        width: 80%;
        color: #565656;
    }
    .explore{
      color:#fff;
      border: 2px solid #3D00B7;
      border-radius: 60px;
      font-weight: 700;
      background-color: #3D00B7;
      padding: 14px 35px;
      margin-top: 30px;
      font-size: 17px;
      transition: .3s all ease-in-out;
      cursor: pointer;
      &:hover{
        background-color: #fff;
        color:#3D00B7;
      }
    }
    .landing-left ul{
        list-style: none;
        padding: 0;
        margin:0;
        display: flex;
        gap: 25px;
        margin-top: 50px;
        li{
            display: flex;
            flex-direction: column;
            span{
                font-size: 40px;
                font-family: 'integral_cfmedium';
                line-height: 1;
                color: #000;
            }
        }
    }
    .landing-left img{
        position: absolute;
        left: -3.2rem;
        bottom:65px;
        z-index: -1;
    }

    .landing-right{
        width: 400px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        padding: 1rem;
        background-size: contain;
        background-position: center;
        background-repeat: no-repeat;
        margin-right: 60px;
        background: url(/src/assets/landing.png);
        height: 440px;
    }
    .crbtw h3{
        font-style: normal;
        font-weight: 700;
        font-size: 28px;
        line-height: 36px;
        letter-spacing: -0.05em;
        color: #FFFFFF;
    }
    .user{
        display: flex;
        justify-content: start;
        align-items: center;
        gap: 10px;
    }
    .user span{
        font-style: normal;
        font-weight: 700;
        font-size: 20px;
        line-height: 26px;

        color: #FFFFFF;
    }
    .currentBit{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px;
        border-radius: 11px;
        color:#fff;
        box-shadow: 0px 3px 5px rgb(0 0 0 / 20%);
        background: rgba(255, 255, 255, 0.2);
        backdrop-filter: blur(25px);
    }
    .currentBit .bit2{
        font-weight: 500;
        font-size: 12px;
        line-height: 16px;
    }
    .currentBit .bit2 span{
        font-style: normal;
        font-weight: 700;
        font-size: 16px;
        margin-top: 5px;
        line-height: 21px;
    }
    .flexbit{
        display: flex;
        gap:10px;
        align-items: center;
    }
    .abosolutePosition{
        position: absolute;
        left:-70px;
        bottom: 90px;
    }
    .bg2{
        position: absolute;
        right: -30px;
        top: 24px;
        z-index: -1;
    }
    .bg3{
        position: absolute;
        right: -60px;
        top: 51px;
        z-index: -2;
    }
</style>