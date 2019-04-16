Question: How do I unshield my coin rewards and get them staking on Linux?


I am in the verus-cli folder on ubuntu 18.04
1) ./verus z_shieldcoinbase "*" my_private_address_without_quotationmarks
this capture all so called coinbases, i.e. mined coins that are not yet staking.
you have to wait 100 blocks (minutes) after receiving them before being able to move them.
wait for a few minutes for the tx to be confirmed.
2)  ./verus z_getbalance my_private_address_without_quotationmarks this is to substract the 0.0001 VRSC fee from the balance in the next step.
3) ./verus z_sendmany my_private_address_without_quotationmarks '[{"address":"my_transaprent_address","amount":95.9998}]'
amount is minus 0.0001 from balance and without quotation marks.
(4) to verify: ./verus z_gettotalbalance
after a few minutes (operations from private addresses are a bit time consuming)

Note: I am always using the same private address.

(submitted by @karero, based on @dukeleto)