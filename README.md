# Telos setramrate

## Background

In order to avoid RAM market speculation at the launch of the Telos blockchain, a significant portion of the blockchain RAM was purchased by the ramlaunch.tf account. This RAM was gradually sold over the past 18 months to ensure a stable RAM price. This initial allocation of RAM has now been sold, necessitating the setting on the blockchain RAM rate to a non-zero rate. Up until September 1 when the final RAM from ramlaunch.tf was sold RAM was sold at a rate on 4096 bytes per minute. It is proposed that the chain RAM rate be set to 64 bytes per block (7 680 per minute). This multi-sig sets the RAM rate to 64 bytes per block.

## Transaction

```
cleos $API push action -sjd eosio setramrate '[64]' -p eosio@active > trx.json
```

## Propose

```
cleos $API multisig propose_trx setramrate signatories.json trx.json southafrica1 -p southafrica1@active
```

## Review

```
cleos $API multisig review southafrica1 setramrate
```

## Approve

```
cleos multisig approve southafrica1 setramrate '{"actor": "<youraccount>", "permission": "active"}' -p <youraccount>@active
```