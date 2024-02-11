
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

When an NFT is minted, its id is set to 0 and we can check its details using 'getMetadataDip721' by typing id:
![1](https://github.com/furkancetinalp/ICP_Hacker-s_Den/assets/99509540/6adf2ae4-1984-413b-8163-929e2bd6ee69)


