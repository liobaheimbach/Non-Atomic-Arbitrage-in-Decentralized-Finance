# Non-Atomic Arbitrage in Decentralized Finance

The aggregate anonymized data set created for the paper Non-Atomic Arbitrage in Decentralized Finance can be found at: https://drive.google.com/file/d/1b3TafqpVzP88VhK9UT8oj49jsHee2yXt/view

The aggregate data set is seperated into five subfolders: 
- blocks contains block level data
    - blockInfo.pkl is a pandas dataframe that contains block level data (e.g., proposer, value, etc.)
- casestudy contains PBS bids and price data for the presented case study
- general contains general data
    - blockTime.pkl is a panads dataframe containing the times blocks were first seen 
    - mevdata.pkl is a pandas dataframe containing the daily number and value of sandwich attacks, cyclic arbitrage and liquidations
- price contains price data for BTC and ETH
- swaps contains non-atomic arbitrage data
    - filteredSwapsWithPrice.pkl is a pandas dataframe containing the non-atomic arbitrage data collected

We further provide the scripts used for the data analysis in the following notebook: analyzeData.ipynb. The data folder needs to be placed in the same directory.

Finally, we provide a mapping for searcher and builder addresses, as well as a list of the cryptocurrencies tracked in the following.


## Builder and Seacher Addresses

We provide a mapping from searcher name to their address below.

| name             | address                                   |
|------------------|-------------------------------------------|
| beaversearcher1  |0xa69babef1ca67a37ffaf7a485dfff3382056e78c |
| beaversearcher2  |0xa57bd00134b2850b2a1c55860c9e9ea100fdd6cf |
| builder1searcher |0x57c1e0c2adf6eecdb135bcf9ec5f23b319be2c94 |
| jumpsearcher     |0x9507c04b10486547584c37bcbd931b2a4fee9a41 |
| rsyncsearcher1   |0x0087bb802d9c0e343f00510000729031ce00bf27 |
| rsyncsearcher2   |0x280027dd00ee0050d3f9d168efd6b40090009246 |
| rsyncsearcher3   |0x51c72848c68a965f66fa7a88855f9f7784502a7f |
| mantasearcher    |0xf8b721bff6bf7095a0e10791ce8f998baa254fd0 |
| searcher1        |0xe8cfad4c75a5e1caf939fd80afcf837dde340a69 |
| searcher2        |0x00000000008c4fb1c916e0c88fd4cc402d935e7d |
| searcher3        |0xd7f3fbe8c72a961a5515203eada59750437fa762 |
| searcher4        |0x000000000dfde7deaf24138722987c9a6991e2d4 |
| searcher5        |0x98c3d3183c4b8a650614ad179a1a98be0a8d6b8e |

Additionally, we also provide a mapping from builder names to their address(es) and public key(s). 

| name                                                 | address                                                          | public key                                                                                                               |
|------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| beaverbuild                                          |0x95222290dd7278aa3ddd389cc1e1d165cc4bafe5              | 0x96a59d355b1f65e270b29981dd113625732539e955a1beeecbc471dd0196c4804574ff871d47ed34ff6d921061e9fc27 <br> 0xb5d883565500910f3f10f0a2e3a031139d972117a3b67da191ff93ba00ba26502d9b65385b5bca5e7c587273e40f2319 <br> 0x8dde59a0d40b9a77b901fc40bee1116acf643b2b60656ace951a5073fe317f57a086acf1eac7502ea32edcca1a900521 <br> 0xaec4ec48c2ec03c418c599622980184e926f0de3c9ceab15fc059d617fa0eafe7a0c62126a4657faf596a1b211eec347 <br> 0xacb407cfb554255db2fbbb320f79bb7f1cc1e8d2dc43324e8e31baafd0836340d49c43eebc51828f53bf6d364f9ac207 <br> 0xa21a2f4807a2bcb6b07c10cea241322e0910c30869c1e4eda686b0d69bdcb74d2a140ef994afcf0bb38e0b960df4d2ee|
| bloXrouteM                                           |0xf2f5c73fa04406b1995e397b55c24ab1f3ea726c              | 0x94aa4ee318f39b56547a253700917982f4b737a49fc3f99ce08fa715e488e673d88a60f7d2cf9145a05127f17dcb7c67 <br> 0x976e63c505050e25b70b39238990c78ddf0948685eb8c5687d17ba5089541f37dd3c45999f2db449eac298b1d4856013 <br> 0x8b8edce58fafe098763e4fabdeb318d347f9238845f22c507e813186ea7d44adecd3028f9288048f9ad3bc7c7c735fba <br> 0xaa1488eae4b06a1fff840a2b6db167afc520758dc2c8af0dfb57037954df3431b747e2f900fe8805f05d635e9a29717b <br> 0xafc9274fe595e8cff421ab9e73b031f0dff707ea1852e2233ff070ef18e3876e25c44a9831c4b5f802653d4678ccc31f|
| bloXrouteR                                           |0x199d5ed7f45f4ee35960cf22eade2076e95b253f              | 0x80c7311597316f871363f8395b6a8d056071d90d8eb27defd14759e8522786061b13728623452740ba05055f5ba9d3d5 <br> 0xb9b50821ec5f01bb19ec75e0f22264fa9369436544b65c7cf653109dd26ef1f65c4fcaf1b1bcd2a7278afc34455d3da6 <br> 0x965a05a1ba338f4bbbb97407d70659f4cea2146d83ac5da6c2f3de824713c927dcba706f35322d65764912e7756103e2|
| blocknative                                          |0xbaf6dc2e647aeb6f510f9e318856a1bcd66c5e19              | 0x8000008a03ebae7d8ab2f66659bd719a698b2e74097d1e423df85e0d58571140527c15052a36c19878018aaebe8a6fea <br> 0x9000009807ed12c1f08bf4e81c6da3ba8e3fc3d953898ce0102433094e5f22f21102ec057841fcb81978ed1ea0fa8246 <br> 0xa66f3abc04df65c16eb32151f2a92cb7921efdba4c25ab61b969a2af24b61508783ceb48175ef252ec9f82c6cdf8d8fd <br> 0xa00000a975dffbd1ef61953ac6c90b52b70eb0188eb9d030774346c9248f81e875f7e8bc56c4bbbda297a9543cfa051d|
| builder0x69                                          |0x690b9a9e9aa1c9db991c7721a92d351db4fac990              | 0x8bc8d110f8b5207e7edc407e8fa033937ddfe8d2c6f18c12a6171400eb6e04d49238ba2b0a95e633d15558e6a706fbe4 <br> 0xb194b2b8ec91a71c18f8483825234679299d146495a08db3bf3fb955e1d85a5fca77e88de93a74f4e32320fc922d3027 <br> 0xa971c4ee4ac5d47e0fb9e16be05981bfe51458f14c06b7a020304099c23d2d9952d4254cc50f291c385d15e7cae0cf9d  <br> 0xa4fb63c2ceeee73d1f1711fadf1c5357ac98cecb999d053be613f469a48f7416999a4da35dd60a7824478661399e6772 <br> 0xb8fceec09779ff758918a849bfe8ab43cea79f6a98320af0af5b030f6a7850fcc5883cb965d02efb10eed1ffa987e899                                                                                                                 |
| builder1                                             |0x473780deaf4a2ac070bbba936b0cdefe7f267dfc              | 0xa1daf0ab37a9a204bc5925717f78a795fa2812f8fba8bda10b1b27c554bd7dedd46775106facd72be748eea336f514e9 <br> 0x89783236c449f037b4ad7bae18cea35014187ec06e2daa016128e736739debeafc5fe8662a0613bc4ca528af5be83b3c |
| flashbots                                            | 0xb64a30399f7F6b0C154c2E7Af0a3ec7B0A5b131a <br> 0xdafea492d9c6733ae3d56b7ed1adb60692c98bc5| 0x81babeec8c9f2bb9c329fd8a3b176032fe0ab5f3b92a3f44d4575a231c7bd9c31d10b6328ef68ed1e8c02a3dbc8e80f9 <br> 0x81beef03aafd3dd33ffd7deb337407142c80fea2690e5b3190cfc01bde5753f28982a7857c96172a75a234cb7bcb994f <br> 0xa1dead01e65f0a0eee7b5170223f20c8f0cbf122eac3324d61afbdb33a8885ff8cab2ef514ac2c7698ae0d6289ef27fc
| mantabuiler                                          |0x5f927395213ee6b95de97bddcb1b2b1c0f16844f              | 0xa0d0dbdf7b5eda08c921dee5da7c78c34c9685db3e39e81eb91da94af29eaa50f1468813c86503bf41b4b51bf772800e <br> 0xb1b734b8dd42b4744dc98ea330c3d9da64b7afc050afed96875593c73937d530a773e35ddc4b480f9d2e1d5ba452a469 <br> 0xb5a688d26d7858b38c44f44568d68fb94f112fc834cd225d32dc52f0277c2007babc861f6f157a6fc6c1dc25bf409046|
| rsyncbuilder                                         |0x1f9090aae28b8a3dceadf281b0f12828e676c326              | 0x978a35c39c41aadbe35ea29712bccffb117cc6ebcad4d86ea463d712af1dc80131d0c650dc29ba29ef27c881f43bd587 <br> 0x83d3495a2951065cf19c4d282afca0a635a39f6504bd76282ed0138fe28680ec60fa3fd149e6d27a94a7d90e7b1fb640 <br> 0xacfdcf458829f4693168a57d0659253069d687682bc64ec130d935ecb6e05ccfb80c138bd3cf53546c86715696612ec8 <br> 0x945fc51bf63613257792926c9155d7ae32db73155dc13bdfe61cd476f1fd2297b66601e8721b723cef11e4e6682e9d87 <br> 0x8aab0ed724d2c7f94af139bd2249ab511f08474ac69e761e56918403c81c358f5f8a6d61c62a86dc4cd7bcad935f49d9 <br> 0x8e6df6e0a9ca3fd89db2aa2f3daf77722dc4fbcd15e285ed7d9560fdf07b7d69ba504add4cc12ac999b8094ff30ed06c|


## Cryptocurrencies 
We provide a list of the 60 cryptocurrencies tracked in this study below. They were chosen based on most interactions on DEXes as well as price information on CEXes. 


| name   | address                                    |
|--------|--------------------------------------------|
| USDC   | 0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48 |
| USDT   | 0xdac17f958d2ee523a2206206994597c13d831ec7 |
| (W)ETH | 0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2 |
| DAI    | 0x6b175474e89094c44da98b954eedeac495271d0f |
| (W)BTC | 0x2260FAC5E5542a773Aa44fBCfeDf7C193bc2C599 |
| LDO    | 0x5a98fcbea516cf06857215779fd812ca3bef1b32 |
| LINK   | 0x514910771af9ca656af840dff83e8264ecf986ca |
| UNI    | 0x1f9840a85d5af5bf1d1762f925bdaddc4201f984 |
| PEPE   | 0x6982508145454ce325ddbe47a25d4ec3d2311933 |
| CRV    | 0xd533a949740bb3306d119cc777fa900ba034cd52 |
| APE    | 0x4d224452801aced8b2f0aebe155379bb5d594381 |
| AAVE   | 0x7fc66500c84a76ad7e9c93437bfc5ac33e2ddae9 |
| MATIC  | 0x7d1afa7b718fb893db30a3abc0cfc608aacfebb0 |
| MKR    | 0x9f8f72aa9304c8b593d555f12ef6589cc3a579a2 |
| SHIB   | 0x95ad61b0a150d79219dcf64e1e6cc01f0b64c4ce |
| QNT    | 0x4a220e6096b25eadb88358cb44068a3248254675 |
| RPL    | 0xd33526068d116ce69f19a9ee46f0bd304f21a51f |
| COMP   | 0xc00e94cb662c3520282e6f5717214004a7f26888 |
| ENS    | 0xc18360217d8f7ab5e7c516566761ea12ce7f9d72 |
| SUSHI  | 0x6b3595068778dd592e39a122f4f5a5cf09c90fe2 |
| SYN    | 0x0f2d719407fdbeff09d87557abb7232601fd9f29 |
| LQTY   | 0x6dea81c8171d0ba574754ef6f8b412f2ed88c54d |
| ILV    | 0x767fe9edc9e0df98e07454847909b5e959d7ca0e |
| SNX    | 0xc011a73ee8576fb46f5e1c5751ca3b9fe0af2a6f |
| ALCX   | 0xdbdb4d16eda451d0503b854cf79d55697f90c8df |
| CVX    | 0x4e3fbd56cd56c3e72c1403e103b45db9da5b9d2b |
| dYdX   | 0x92d6c1e31e14520e676a687f0a93788b716beff5 |
| 1INCH  | 0x111111111117dc0aa78b770fa6a738034120c302 |
| AGIX   | 0x5b7533812759b45c2b44c19e320ba2cd2681b542 |
| FXS    | 0x3432b6a60d23ca0dfca7761b7ab56459d9c964d0 |
| SPELL  | 0x090185f2135308bad17527004364ebcc2d37e5f6 |
| YFI    | 0x0bc529c00c6401aef6d220be8c6ea1667f6ad93e |
| BAT    | 0x0d8775f648430679a709e98d2b0cb6250d2887ef |
| GALA   | 0x15d4c048f83bd7e37d49ea4c83a07267ec4203da |
| WLD    | 0x163f8c2467924be0ae7b5347228cabf260318753 |
| CREAM  | 0x2ba592f78db6436527729929aaf6c908497cb200 |
| REN    | 0x408e41876cccdc0f92210600ef50372656052a38 |
| FTM    | 0x4e15361fd6b4bb609fa63c81a2be19d873717870 |
| RNDR   | 0x6de037ef9ad2725eb40118bb1702ebb27e4aeb24 |
| OGN    | 0x8207c1ffc5b6804f6024322ccf34f29c3541ae26 |
| NEXO   | 0xb62132e35a6c13ee1ee0f84dc5d40bad8d815206 |
| PERP   | 0xbc396689893d065f41bc2c6ecbee5e0085233447 |
| IMX    | 0xf57e7e7c23978c3caec3c3548e3d615c346e79ff |
| MANA   | 0x0f5d2fb29fb7d3cfee444a200298f468908cc942 |
| KP3R   | 0x1ceb5cb57c4d4e2b2433641b95dd330a33185a44 |
| YGG    | 0x25f8087ead173b73d6e8b84329989a8eea16cf73 |
| ID     | 0x2dff88a56767223a5529ea5960da7a3f5f766406 |
| SAND   | 0x3845badade8e6dff049820680d1f14bd3903a5d0 |
| BLUR   | 0x5283d291dbcf85356a21ba090e6db59121208b44 |
| OCEAN  | 0x967da4048cd07ab37855c090aaf366e4ce1b9f48 |
| stETH  | 0xae7ab96520de3a18e5e111b5eaab095312d7fe84 |
| FET    | 0xaea46a60368a7bd060eec7df8cba43b7ef41ad85 |
| PRIME  | 0xb23d80f5fefcddaa212212f028021b41ded428cf |
| HFT    | 0xb3999f658c0391d94a37f7ff328f3fec942bcadc |
| BAND   | 0xba11d00c5f74255f56a5e366f4f77f5a186d7f55 |
| GRT    | 0xc944e90c64b2c07662a292be6244bdf05cda44a7 |
| GALA   | 0xd1d2eb1b1e90b638588728b4130137d262c87cae |
| ZRX    | 0xe41d2489571d322189246dafa5ebde1f4699f498 |
| GALA   | 0xd1d2eb1b1e90b638588728b4130137d262c87cae |
| ENJ    | 0xf629cbd94d3791c9250152bd8dfbdf380e2a3b9c |
| HEX    | 0x2b591e99afe9f32eaa6214f7b7629768c40eeb39 |
