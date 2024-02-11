
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
