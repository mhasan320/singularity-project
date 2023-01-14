<template>
    <div class="placeBit">
        <div class="singleBit">
            <img src="../assets/landing.png" alt="bit"/>
            <div class="futr">
                <div class="singlftr">
                    <img src="../assets/user.png" alt="user"/>
                    <div>
                        <h4>The Futr Abstr</h4>
                        <p>10 in the stock</p>
                    </div>
                </div>
                <div class="singlerftr">
                    <p>Highest Bid</p>
                    <div class="single__Item">
                        <IconEthurm/>
                        0.25 ETH
                    </div>
                </div>
            </div>
        </div>
        <div class="singleBit">
            <div class="singleftr">
                <img src="../assets/bg2.png" alt="futr">
                <div class="ftrbase">
                    <h3>The Futr Abstr</h3>
                    <div class="ftrspan">
                        <img src="../assets/user.png" alt="user"/>
                        <div class="ettext">
                            <IconEthurm/>
                            0.25 ETH
                        </div>
                        1 of 8
                    </div>
                    <button class="btn-seccound">Place a bid</button>
                </div>
            </div>
            <div class="singleftr">
                <img src="../assets/bg2.png" alt="futr">
                <div class="ftrbase">
                    <h3>The Futr Abstr</h3>
                    <div class="ftrspan">
                        <img src="../assets/user.png" alt="user"/>
                        <div class="ettext">
                            <IconEthurm/>
                            0.25 ETH
                        </div>
                        1 of 8
                    </div>
                    <button class="btn-seccound">Place a bid</button>
                </div>
            </div>
            <div class="singleftr">
                <img src="../assets/bg2.png" alt="futr">
                <div class="ftrbase">
                    <h3>The Futr Abstr</h3>
                    <div class="ftrspan">
                        <img src="../assets/user.png" alt="user"/>
                        <div class="ettext">
                            <IconEthurm/>
                            0.25 ETH
                        </div>
                        1 of 8
                    </div>
                    <button class="btn-seccound">Place a bid</button>
                </div>
            </div>
        </div>
        <div class="signleBit collection">
            <h3 class="text">Top collection Over</h3>
            <h4>Last 7 days</h4>
            <ul>
                <li v-for="collection in collectionsArray" class="list-item" :key="collection.id">
                    <span class="collectionId">{{collection.id}}</span>
                    <div class="userItem">
                        <img :src="collection.img" alt="item" />
                        <span v-if="collection.activeIcon">
                            <img :src="collection.activeIcon" alt="item" />
                        </span>
                    </div>
                    <div class="itemSection">
                        <h3>{{collection.title}}</h3>
                        <span>
                            <svg width="13" height="22" viewBox="0 0 13 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <g clip-path="url(#clip0_0_213)">
                                <path d="M12.671 11.4564L6.50004 15.3231L0.325043 11.4564L6.50004 0.589722L12.671 11.4564ZM6.50004 16.5647L0.325043 12.6981L6.50004 21.9231L12.675 12.6981L6.50004 16.5647Z" fill="#3A3A3A"/>
                                </g>
                                <defs>
                                <clipPath id="clip0_0_213">
                                <rect width="13" height="21.3333" fill="white" transform="translate(0 0.589722)"/>
                                </clipPath>
                                </defs>
                            </svg>
                            <p>{{ collection.ethurm }}</p>
                        </span>
                    </div>
                    <div v-if="collection.redPer === true" class="perRed">{{collection.percentage}}%</div>
                    <div v-else class="percentage">{{collection.percentage}}%</div>
                </li>
            </ul>
        </div>
    </div>
    </template>
    
    <script>
        import IconEthurm from "./icons/IconEthurm.vue"
        import userImg from "../assets/criptlo.png"
        import ActiveIcon from "../assets/verify.png"
        export default {
            data: function() {
                return {
                    collectionsArray: [{
                        id: 1,
                        img: userImg,
                        etum: IconEthurm,
                        activeIcon: null,
                        title: 'CrytoFunks',
                        ethurm: '19,769.45',
                        percentage: '+ 26.52',
                        redPer: false
                    },
                    {
                        id: 2,
                        img: userImg,
                        etum: IconEthurm,
                        activeIcon: ActiveIcon,
                        title: 'CrytoFunks',
                        ethurm: '11,769.45',
                        percentage: '+ 20.52',
                        redPer: false
                    },
                    {
                        id: 3,
                        img: userImg,
                        etum: IconEthurm,
                        activeIcon: null,
                        title: 'Frensware',
                        ethurm: '19,769.45',
                        percentage: '+ 26.52',
                        redPer: false
                    },
                    {
                        id: 4,
                        img: userImg,
                        etum: IconEthurm,
                        activeIcon: ActiveIcon,
                        title: 'PunkArt',
                        ethurm: '19,769.45',
                        percentage: '+ 26.52',
                        redPer: false,
                    },
                    {
                        id: 5,
                        img: userImg,
                        etum: IconEthurm,
                        activeIcon: null,
                        title: 'CrytoFunks',
                        ethurm: '19,769.45',
                        percentage: '+ 26.52',
                        redPer: true,
                    }]
                };
            },
            methods:{
                Msg:function(){
                    return '$' + this.title
                }
            }
        }
    </script>
    
    <style scoped lang="scss">
        .placeBit{
            padding: 5rem 5rem;
            gap: 30px;
            display: flex;
            justify-content: space-between;
        }
        .signleBit{
            width: 33.33%;
        }
        .futr, .singlftr, .singleftr{
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .futr{
            margin-top: 20px;
        }
        .singlftr{
            gap: 15px;
        }
        .singlftr h4{
            font-style: normal;
            font-weight: 700;
            font-size: 20px;
            line-height: 26px;
        }
        .singlftr p{
            font-style: normal;
            font-weight: 500;
            font-size: 12px;
            line-height: 16px;
        }
        .single__Item{
            font-style: normal;
            font-weight: 700;
            font-size: 16px;
            line-height: 21px;
        }
        .singleftr img{
            width: 130px;
        }
        .singleftr{
            gap: 20px;
            margin-bottom: 40px;
        }
        .ftrspan{
            display: flex;
            gap:10px;
            align-items: center;
        }
        .ftrspan img{
            width: 50px !important;
        }
        .ettext{
            border:1px solid green;
            color: green;
            padding: 3px 5px;
            border-radius: 5px;
        }
        .btn-seccound{
        color:#3D00B7;
        border: 2px solid #3D00B7;
        border-radius: 25px;
        font-weight: 500;
        background-color: transparent;
        padding: 12px 15px;
        margin-top: 10px;
        transition: .3s all ease-in-out;
        cursor: pointer;
        &:hover{
            background-color: #3D00B7;
            color:#fff;
        }
        }
        .collection h3.text{
            font-style: normal;
            font-weight: 700; 
            font-family: 'integral_cfmedium';
            font-size: 20px;
            line-height: 24px;
        }
        .collection h4{
            font-style: normal;
            font-weight: 700;
            font-size: 18px;
            line-height: 23px;
            margin-top: 5px;
            margin-bottom: 20px;
            color: #3D00B7;
        }
        .collection ul{
            list-style: none;
            padding: 0px;
            margin: 0px;
        }
        .collection ul li{
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 10px;
            padding: 4px 0px;
            border-bottom: 1px solid #ccc;
        }
        .userItem{
            position: relative;
        }
        .userItem span{
            position: absolute;
            right: -10px;
            top: -7px;
        }
        .itemSection h3{
            font-style: normal;
            font-weight: 500;
            font-size: 16px;
            line-height: 103%;
        }
        .itemSection span{
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 10px;
        }
        .percentage, .perRed{
            font-style: normal;
            font-weight: 600;
            font-size: 20px;
            line-height: 103%;
            color: #14C8B0;
        }
        .collectionId{
            font-style: normal;
            font-weight: 700;
            font-size: 24px;
            line-height: 103%;
        }
        .perRed{
            color: red !important;
        }
    </style>