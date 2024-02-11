
To Deploy

```
fx deploy --argument 'record{name="DFX Blobs";symbol="DFXB";custodians=null;logo=null}' dip721_nft_container

```




To Mint
```
dfx canister call dip721_nft_container mintDip721 \
    "(principal\"kopdi-nmhgu-x6de7-2iktk-7ylbn-422aq-u4w5b-dfneu-lxxb4-yzu4j-tqe\",vec{record{
        purpose=variant{Rendered};
        data=blob\"hello\";
        city=\"Istanbul\";
        weather_condition = variant{Snow};
        key_val_data=vec{
            record{
                \"contentType\";
                variant{TextContent=\"text/plain\"};
            };
            record{
                \"locationType\";
                variant{Nat8Content=4:nat8}
            };
        }
    }},blob\"hello\")"
(variant { Ok = record { id = 0 : nat; token_id = 0 : nat64 } })
```
After deploying and minting NFT, we can check the NFT and its info using whether id or principal:

When an NFT is minted, its id is assigned as 0 (because it is the first NFT) and we can check its details using 'getMetadataDip721' by typing id:


![1](https://github.com/furkancetinalp/ICP_Hacker-s_Den/assets/99509540/6adf2ae4-1984-413b-8163-929e2bd6ee69)

We can also see details using 'getMetadataForUserDip721' method using principal:

![4](https://github.com/furkancetinalp/ICP_Hacker-s_Den/assets/99509540/7b33e6f0-bf96-43fd-beb0-bfa139195ed8)


As we can see, we added city and weather condition into our NFT.
To see the city of related NFT, we can use 'getCity' method by typing id:

![2](https://github.com/furkancetinalp/ICP_Hacker-s_Den/assets/99509540/c764a690-390f-43ab-b65b-75f2b32f528f)

To see the weather conditiob of related NFT, we can use 'getWeatherCondition' method by typing id:

![3](https://github.com/furkancetinalp/ICP_Hacker-s_Den/assets/99509540/269e29d4-258b-4e4e-9cee-8587e6e02108)


