# qrlwallet.proto



## AddAddressFromSeedReq



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| seed | [string](#string) |  |  |





## AddAddressFromSeedResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| address | [string](#string) |  |  |





## AddNewAddressReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| height | [uint64](#uint64) |  | Seed can be either hexseed or mnemonic |
| hash_function | [string](#string) |  |  |


## AddNewAddressResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| address | [string](#string) |  |  |


## BalanceReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| address | [string](#string) |  |  |


## BalanceResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| balance | [uint64](#uint64) |  |  |



## BlockByNumberReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| block_number | [uint64](#uint64) |  |  |



## BlockReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| header_hash | [string](#string) |  |  |



## BlockResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| block | [Block](#qrl.Block) |  |  |




## ChangePassphraseReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| oldPassphrase | [string](#string) |  |  |
| newPassphrase | [string](#string) |  |  |


## ChangePassphraseResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |


## EncryptWalletReq


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| passphrase | [string](#string) |  |  |


## EncryptWalletResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |


## GetRecoverySeedsReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| address | [string](#string) |  |  |


## GetRecoverySeedsResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| hexseed | [string](#string) |  |  |
| mnemonic | [string](#string) |  |  |



## GetWalletInfoReq



## GetWalletInfoResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| version | [uint32](#uint32) |  |  |
| address_count | [uint64](#uint64) |  |  |
| is_encrypted | [bool](#bool) |  |  |


## HeightReq

## HeightResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| height | [uint64](#uint64) |  |  |


## ListAddressesReq

## ListAddressesResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| addresses | [string](#string) | repeated |  |


## LockWalletReq

## LockWalletResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |


## OTSReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| address | [string](#string) |  |  |


## OTSResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| ots_bitfield | [bytes](#bytes) | repeated |  |
| next_unused_ots_index | [uint64](#uint64) |  |  |


## RelayMessageTxnReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| message | [string](#string) |  |  |
| fee | [uint64](#uint64) |  |  |
| master_address | [string](#string) |  |  |
| signer_address | [string](#string) |  |  |
| ots_index | [uint64](#uint64) |  |  |


## RelaySlaveTxnReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| slave_pks | [bytes](#bytes) | repeated |  |
| access_types | [uint32](#uint32) | repeated |  |
| fee | [uint64](#uint64) |  |  |
| master_address | [string](#string) |  |  |
| signer_address | [string](#string) |  |  |
| ots_index | [uint64](#uint64) |  |  |


## RelayTokenTxnReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| symbol | [string](#string) |  |  |
| name | [string](#string) |  |  |
| owner | [string](#string) |  |  |
| decimals | [uint64](#uint64) |  |  |
| addresses | [string](#string) | repeated |  |
| amounts | [uint64](#uint64) | repeated |  |
| fee | [uint64](#uint64) |  |  |
| master_address | [string](#string) |  |  |
| signer_address | [string](#string) |  |  |
| ots_index | [uint64](#uint64) |  |  |


## RelayTransferTokenTxnReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| addresses_to | [string](#string) | repeated |  |
| token_txhash | [string](#string) |  |  |
| amounts | [uint64](#uint64) | repeated |  |
| fee | [uint64](#uint64) |  |  |
| master_address | [string](#string) |  |  |
| signer_address | [string](#string) |  |  |
| ots_index | [uint64](#uint64) |  |  |


## RelayTransferTxnReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| addresses_to | [string](#string) | repeated |  |
| amounts | [uint64](#uint64) | repeated |  |
| fee | [uint64](#uint64) |  |  |
| master_address | [string](#string) |  |  |
| signer_address | [string](#string) |  |  |
| ots_index | [uint64](#uint64) |  |  |


## RelayTxnResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| tx | [Transaction](#qrl.Transaction) |  |  |



## RemoveAddressReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| address | [string](#string) |  |  |


## RemoveAddressResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |


## TransactionReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| tx_hash | [string](#string) |  |  |



## TransactionResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| tx | [Transaction](#qrl.Transaction) |  |  |
| confirmations | [uint64](#uint64) |  |  |



## TransactionsByAddressReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| address | [string](#string) |  |  |



## TransactionsByAddressResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
| mini_transactions | [MiniTransaction](#qrl.MiniTransaction) | repeated |  |
| balance | [uint64](#uint64) |  |  |


## UnlockWalletReq

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| passphrase | [string](#string) |  |  |


## UnlockWalletResp

| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [uint32](#uint32) |  |  |
| error | [string](#string) |  |  |
