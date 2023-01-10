
<!-- logo -->
<p align="center">
  <img width='400' src="img/logo.jpg">
</p>

<!-- tag line -->
<h3 align='center'> Python package for Defi Protocols! </h3>

## 🌻 Motivation

 Karpatkey tech team has always been dealing with defi protocols for various purposes, like getting prices, underlying tokens, pools, rewards, alerts, fees, reporting, APRs, etc. As a result of this search we created this protocol with all the knowledge acquired to contribute to the web3 and DEFI community. We hope it will be useful for your developments!


## Repo Url

[KarpatkeyDAO/defi-protocols](https://github.com/KarpatkeyDAO/defi-protocols)


## Installing from repository

```bash
pip3 install git+https://github.com/KarpatkeyDAO/defi-protocols.git#egg=defi_protocols
```

## Installing latest version available on pypi

[pip3 install defi-protocols](https://pypi.org/project/defi-protocols/0.0.1/)


## Config 

- First you will have to modify the [config.json](https://github.com/KarpatkeyDAO/defi-protocols/blob/dev/defi_protocols/config.json) and place under `/path/to/python/site-packages/defi-protocols/config.json`

- You should provide `RPC` endpoints and `EXPLORER API KEYS`


## Protocols supported


| Protocol      | Underlying | Rewards | Fees |
|---------------|------------|---------|------|
| AAVE          | ✔          | ✔       |  -   |
| Agave         | ✔          | ✔       |  -   |
| Aura          | ✔          | ✔       |  -   |
| Balancer      | ✔          | ✔       |  -   |
| Bancor        | ✔          | ?       |  -   |
| Convex        | ✔          | ✔       |  -   |
| Curve         | ✔          | ✔       |  -   |
| Elk           | ✔          | ✔       |  -   |
| Honeyswap     | ✔          | -       |  -   |
| Maker         | ✔          | -       |  -   |
| QiDao         | ✔          | -       |  -   |
| SushiSwap     | ✔          | ✔       |  -   |
| Swapr         | ✔          | ✔       |  -   |
| Symmetric     | ✔          | ✔       |  -   |
| Unit Protocol | ✔          | ✔       |  -   |
| Uniswap V3    | ✔          | ?       |  -   |
| Compound      | ✔          | pending |  -   |


## Docs

- <details><summary><b>Functions</b></summary>

  # Functions

  ## Defined in functions.py


  ### 1: get_node(blockchain, block='latest', index=0)

  > Description: function returns web3 object of the node

  - <details><summary><b>Example</b></summary>

    ```
    a = get_node(ETHEREUM, 'latest', 0)
    print(a)
    ```

    ```
    output:
    <web3.main.Web3 object at 0x7fe8c584b8b0>
    ```
    </details>

  ### 2: last_block(blockchain, web3=None, block='latest', index=0)

  > Description: functoion returns last block of the blockchain

  - <details><summary><b>Example</b></summary>

    ```
    a = last_block(ETHEREUM, None, 'latest', 0)
    print(a)
    ```

    ```
    output:
    16370420
    ```
    </details>

  ### 3: timestamp_to_date(timestamp, utc=0)

  > Description: function retuns timestamp to date conversion

  - <details><summary><b>Example</b></summary>

    ```
    a = timestamp_to_date(1663181616)
    print(a)
    ```

    ```
    output:
    2022-09-14 18:53:36
    ```
    </details>

  ### 4: timestamp_to_block(timestamp, blockchain) -> int

  > Description: function returns timestamp to block conversion

  - <details><summary><b>Example</b></summary>

    ```
    a = timestamp_to_block(1663181616, ETHEREUM)
    print(a)
    ```

    ```
    output:
    15534540
    ```
    </details>

  ### 5: date_to_timestamp(datestring, utc=0)

  > Description: function returns date to timestamp conversion

  - <details><summary><b>Example</b></summary>

    ```bash
    a = date_to_timestamp('2022-01-14 00:00:00')
    print(a)
    ```

    ```
    output:
    1642118400
    ```
    </details>

  ### 6: date_to_block(datestring, blockchain, utc=0) -> int

  > Description: function returns date to block conversion

  - <details><summary><b>Example</b></summary>

    ```bash
    a = date_to_block('2022-01-14 00:00:00', ETHEREUM)
    print(a)

    ```

    ```
    output:
    14000270
    ```
    </details>

  ### 7: block_to_timestamp(block, blockchain)

  > Description: function returns block to timestamp conversion

  - <details><summary><b>Example</b></summary>

    ```bash
    a = block_to_timestamp(14000200, ETHEREUM)
    print(a)

    ```

    ```
    output:
    1642117536
    ```
    </details>

  ### 8: block_to_date(block, blockchain, utc=0)

  > Description: function returns block to date conversion

  - <details><summary><b>Example</b></summary>

    ```bash
    a = block_to_date(14000270, ETHEREUM)
    print(a)

    ```

    ```
    output:
    2022-01-13 23:59:54
    ```
    </details>

  ### 9: get_blocks_per_year(blockchain)

  > Description: function returns blocks per year for a blockchain

  - <details><summary><b>Example</b></summary>

    ```bash
    a = get_blocks_per_year(ETHEREUM)
    print(a)

    ```

    ```
    output:
    2398217
    ```
    </details>

  ### 10: token_info(token_address, blockchain)

  > Description: function returns token related info

  - <details><summary><b>Example</b></summary>

    ```bash
    a = token_info('0x6810e776880C02933D47DB1b9fc05908e5386b96', ETHEREUM)
    print (a)

    ```

    ```
    output:
    {'address': '0x6810e776880c02933d47db1b9fc05908e5386b96', 'name': 'Gnosis', 'decimals': '18', 'symbol': 'GNO', 'totalSupply': '10000000000000000000000000', 'owner': '', 'txsCount': 154486, 'transfersCount': 318423, 'lastUpdated': 1673304547, 'issuancesCount': 0, 'holdersCount': 16650, 'website': 'https://gnosis.pm/', 'image': '/images/GNO6810e776.png', 'ethTransfersCount': 0, 'price': {'rate': 91.2045572764551, 'diff': 4, 'diff7d': 8.78, 'ts': 1673304180, 'marketCapUsd': 236182227.06842083, 'availableSupply': 2589588, 'volume24h': 1954362.90295114, 'volDiff1': 17.234718455656363, 'volDiff7': 1358.516624011187, 'volDiff30': 108.75660649607727, 'diff30d': 1.367903603382814, 'bid': 323.4, 'currency': 'USD'}, 'publicTags': ['DEX', 'Protocol', 'DeFi'], 'countOps': 318423}
    ```
    </details>

  ### 11: balance_of(address, contract_address, block, blockchain, execution=1, web3=None, index=0, decimals=True)

  > Description: function returns ballance of given wallet for given contract

  - <details><summary><b>Example</b></summary>

    ```bash
    a = balance_of('0x2D0669DB84f11A9EAD41e57Ce2f242D92111a58F', '0x6810e776880C02933D47DB1b9fc05908e5386b96', 'latest', ETHEREUM)
    print(a)

    ```

    ```
    output:
    0.0
    ```
    </details>

  ### 12: total_supply(token_address, block, blockchain, execution=1, web3=None, index=0, decimals=True)

  > Description: fucntion returns total suppy for a given token contract address

  - <details><summary><b>Example</b></summary>

    ```bash
    a = total_supply('0x6810e776880C02933D47DB1b9fc05908e5386b96', 'latest', ETHEREUM)
    print(a)

    ```

    ```
    output:
    10000000.0
    ```
    </details>

  ### 13: get_decimals(token_address, blockchain, execution=1, web3=None, block='latest', index=0)

  > Description: function returns decimals for given token address


  ### 14: get_symbol(token_address, blockchain, execution=1, web3=None, block='latest', index=0) -> str

  > Description: function returns symbol for given toke contract address

  ### 15: get_contract_abi(contract_address, blockchain)

  > fucntion returns abi for given contract address

  ### 16: get_contract(contract_address, blockchain, web3=None, abi=None, block='latest', index=0)

  > Description: function returns web3 contract object for given contract object

  - <details><summary><b>Example</b></summary>

    ```bash
    print(get_contract('0xdAC17F958D2ee523a2206206994597C13D831ec7', ETHEREUM))

    ```

    ```
    output:
    <web3._utils.datatypes.Contract object at 0x7f1dfdcb7af0>
    ```
    </details>

  ### 16: get_contract_proxy_abi(contract_address, abi_contract_address, blockchain, web3=None, block='latest', index=0)

  > Description: function returns abi for given contract with the help of proxy conract

  - <details><summary><b>Example</b></summary>

    ```bash
    # a = get_contract_abi('0xdc31ee1784292379fbb2964b3b9c4124d8f89c60', GOERLI)

    # print(a)

    b = get_contract_proxy_abi('0xdc31ee1784292379fbb2964b3b9c4124d8f89c60', '0xe2E52C2D0D64209b8DD1854371A4C673c13448f0', GOERLI)

    print(b)
    ```

    ```
    output:
    <web3._utils.datatypes.Contract object at 0x7f61efe07af0>
    ```
    </details>

  ### 17: search_proxy_contract(contract_address, blockchain, web3=None)

  > Description: function returns proxy contracts for given contract

  - <details><summary><b>Example</b></summary>

    ```bash
    d = search_proxy_contract('0x4aa42145Aa6Ebf72e164C9bBC74fbD3788045016', XDAI)

    print(d)

    ```

    ```
    output:
    <web3._utils.datatypes.Contract object at 0x7f0ac475ba90>
    ```
    </details>

  ### 18: get_abi_function_signatures(contract_address, blockchain, web3=None, abi_address=None)

  > Description: function returns function signatures for givenn contract address

  - <details><summary><b>Example</b></summary>

    ```bash
    d = get_abi_function_signatures('0x4aa42145Aa6Ebf72e164C9bBC74fbD3788045016', XDAI)

    print(d)

    ```

    ```
    output:
    [{'name': 'claimValues', 'signature': 'claimValues(address,address)', 'inline_signature': 'claimValues(address,address)', 'components': ['address', 'address'], 'stateMutability': 'nonpayable'}, {'name': 'owner', 'signature': 'owner()', 'inline_signature': 'owner()', 'components': [], 'stateMutability': 'view'}, {'name': 'transferOwnership', 'signature': 'transferOwnership(address)', 'inline_signature': 'transferOwnership(address)', 'components': ['address'], 'stateMutability': 'nonpayable'}]
    ```
    </details>

  ### 19: get_data(contract_address, function_name, parameters, blockchain, web3=None, abi_address=None)

  > Description: function returns data of a specific function of given contract address

  - <details><summary><b>Example</b></summary>

    ```bash
    d = get_data('0x4aa42145Aa6Ebf72e164C9bBC74fbD3788045016', 'owner', None, XDAI)

    print(d)

    ```

    ```
    output:
    0x8da5cb5b
    ```
    </details>

  ### 20: get_token_tx(token_address, contract_address, block_start, block_end, blockchain)

  > Description: function returns transactions on given contract for given token address for given block range

  - <details><summary><b>Example</b></summary>

    ```bash
    e = get_token_tx('0x4ECaBa5870353805a9F068101A40E0f32ed605C6', '0xc30141B657f4216252dc59Af2e7CdB9D8792e1B0', 25813406, 'latest', XDAI)

    print(e)

    ```

    ```
    output:
    [{'blockNumber': '25848427', 'timeStamp': '1673114785', 'hash': '0x75a397e95e3e5761b21f05ead73834455fda37888ec27079a8f1a45b24b6d1cb', 'nonce': '686', 'blockHash': '0x7f818d65d54f4a00ae968965a13d5d7cd113b67f0fba326d674cefa3ec8bb2b6', 'from': '0xc30141b657f4216252dc59af2e7cdb9d8792e1b0', 'contractAddress': '0x4ecaba5870353805a9f068101a40e0f32ed605c6', 'to': '0xac313d7491910516e06fbfc2a0b5bb49bb072d91', 'value': '101454525', 'tokenName': 'Tether USD on xDai', 'tokenSymbol': 'USDT', 'tokenDecimal': '6', 'transactionIndex': '1', 'gas': '926025', 'gasPrice': '1825346000', 'gasUsed': '562326', 'cumulativeGasUsed': '583326', 'input': 'deprecated', 'confirmations': '36987'}, {'blockNumber': '25848427', 'timeStamp': '1673114785', 'hash': '0x75a397e95e3e5761b21f05ead73834455fda37888ec27079a8f1a45b24b6d1cb', 'nonce': '686', 'blockHash': '0x7f818d65d54f4a00ae968965a13d5d7cd113b67f0fba326d674cefa3ec8bb2b6', 'from': '0x1111111254fb6c44bac0bed2854e76f90643097d', 'contractAddress': '0x4ecaba5870353805a9f068101a40e0f32ed605c6', 'to': '0xc30141b657f4216252dc59af2e7cdb9d8792e1b0', 'value': '101454525', 'tokenName': 'Tether USD on xDai', 'tokenSymbol': 'USDT', 'tokenDecimal': '6', 'transactionIndex': '1', 'gas': '926025', 'gasPrice': '1825346000', 'gasUsed': '562326', 'cumulativeGasUsed': '583326', 'input': 'deprecated', 'confirmations': '36987'}, {'blockNumber': '25842520', 'timeStamp': '1673084125', 'hash': '0x521a6ed38b407d3101456135fdae3428e5ce32eb6749ed8bee1beeb28591bb79', 'nonce': '471', 'blockHash': '0x322acd3bad3b462d053e014c088b164c7d17491d683d946d7edb4f7374bc14c4', 'from': '0xc30141b657f4216252dc59af2e7cdb9d8792e1b0', 'contractAddress': '0x4ecaba5870353805a9f068101a40e0f32ed605c6', 'to': '0xac313d7491910516e06fbfc2a0b5bb49bb072d91', 'value': '36272803', 'tokenName': 'Tether USD on xDai', 'tokenSymbol': 'USDT', 'tokenDecimal': '6', 'transactionIndex': '5', 'gas': '828950', 'gasPrice': '2000000007', 'gasUsed': '535324', 'cumulativeGasUsed': '886617', 'input': 'deprecated', 'confirmations': '42894'}, {'blockNumber': '25842520', 'timeStamp': '1673084125', 'hash': '0x521a6ed38b407d3101456135fdae3428e5ce32eb6749ed8bee1beeb28591bb79', 'nonce': '471', 'blockHash': '0x322acd3bad3b462d053e014c088b164c7d17491d683d946d7edb4f7374bc14c4', 'from': '0x1111111254fb6c44bac0bed2854e76f90643097d', 'contractAddress': '0x4ecaba5870353805a9f068101a40e0f32ed605c6', 'to': '0xc30141b657f4216252dc59af2e7cdb9d8792e1b0', 'value': '36272803', 'tokenName': 'Tether USD on xDai', 'tokenSymbol': 'USDT', 'tokenDecimal': '6', 'transactionIndex': '5', 'gas': '828950', 'gasPrice': '2000000007', 'gasUsed': '535324', 'cumulativeGasUsed': '886617', 'input': 'deprecated', 'confirmations': '42894'}, {'blockNumber': '25814478', 'timeStamp': '1672938840', 'hash': '0x48c01f261497eb2ab9a82dfd019d4d019b7d5bd9707399e1ae8ec0891542bf29', 'nonce': '3132', 'blockHash': '0xcb1b78d76b7ca57c8feaff09862662d071a9fefe435e7dc7baf14e5b954ac45b', 'from': '0xc30141b657f4216252dc59af2e7cdb9d8792e1b0', 'contractAddress': '0x4ecaba5870353805a9f068101a40e0f32ed605c6', 'to': '0xac313d7491910516e06fbfc2a0b5bb49bb072d91', 'value': '48987164', 'tokenName': 'Tether USD on xDai', 'tokenSymbol': 'USDT', 'tokenDecimal': '6', 'transactionIndex': '1', 'gas': '1007940', 'gasPrice': '1500000007', 'gasUsed': '610897', 'cumulativeGasUsed': '802730', 'input': 'deprecated', 'confirmations': '70936'}, {'blockNumber': '25814478', 'timeStamp': '1672938840', 'hash': '0x48c01f261497eb2ab9a82dfd019d4d019b7d5bd9707399e1ae8ec0891542bf29', 'nonce': '3132', 'blockHash': '0xcb1b78d76b7ca57c8feaff09862662d071a9fefe435e7dc7baf14e5b954ac45b', 'from': '0x1111111254fb6c44bac0bed2854e76f90643097d', 'contractAddress': '0x4ecaba5870353805a9f068101a40e0f32ed605c6', 'to': '0xc30141b657f4216252dc59af2e7cdb9d8792e1b0', 'value': '48987164', 'tokenName': 'Tether USD on xDai', 'tokenSymbol': 'USDT', 'tokenDecimal': '6', 'transactionIndex': '1', 'gas': '1007940', 'gasPrice': '1500000007', 'gasUsed': '610897', 'cumulativeGasUsed': '802730', 'input': 'deprecated', 'confirmations': '70936'}]
    ```
    </details>

  ### 21: get_tx_list(contract_address, block_start, block_end, blockchain)

  > Description: function returns txs list for given contract address for given block range


  - <details><summary><b>Example</b></summary>

    ```bash
    e = get_tx_list('0x4ECaBa5870353805a9F068101A40E0f32ed605C6', 25884100, 'latest', XDAI)

    print(e)

    ```

    ```
    output:
    [{'blockNumber': '25884304', 'timeStamp': '1673301985', 'hash': '0x2eb63c1d0af69b41969515885badb605a791a1ae4917339d895294ec88b8c4c2', 'nonce': '3', 'blockHash': '0x1f5189238d55e31fd9510022a3a50d0649f5a8110601ed138f4661a1de862460', 'transactionIndex': '41', 'from': '0x10e35f286bc156272c6846b97d1a95b9555ced4b', 'to': '0x4ecaba5870353805a9f068101a40e0f32ed605c6', 'value': '0', 'gas': '289343', 'gasPrice': '2910000001', 'isError': '1', 'txreceipt_status': '0', 'input': '0x4000aea0000000000000000000000000f6a78083ca3e2a662d6dd1703c939c8ace2e268d00000000000000000000000000000000000000000000000000000000124616160000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000001410e35f286bc156272c6846b97d1a95b9555ced4b000000000000000000000000', 'contractAddress': '', 'cumulativeGasUsed': '3381775', 'gasUsed': '30207', 'confirmations': '1169', 'methodId': '0x4000aea0', 'functionName': 'transferAndCall(address _to, uint256 _value, bytes _data)'}, {'blockNumber': '25884303', 'timeStamp': '1673301980', 'hash': '0x75b29da1b0ea555d70955ebeacc2797e46f60deb6540805ed68a6585c78f8699', 'nonce': '2', 'blockHash': '0x32044065f599e8c4f4c5fb9ce3e17b0d3633678b10b462e0bd3417a0caaf9636', 'transactionIndex': '0', 'from': '0x10e35f286bc156272c6846b97d1a95b9555ced4b', 'to': '0x4ecaba5870353805a9f068101a40e0f32ed605c6', 'value': '0', 'gas': '289343', 'gasPrice': '2910000001', 'isError': '0', 'txreceipt_status': '1', 'input': '0x4000aea0000000000000000000000000f6a78083ca3e2a662d6dd1703c939c8ace2e268d00000000000000000000000000000000000000000000000000000000124616160000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000001410e35f286bc156272c6846b97d1a95b9555ced4b000000000000000000000000', 'contractAddress': '', 'cumulativeGasUsed': '227528', 'gasUsed': '227528', 'confirmations': '1170', 'methodId': '0x4000aea0', 'functionName': 'transferAndCall(address _to, uint256 _value, bytes _data)'}]
    ```
    </details>

  ### 22: get_logs(block_start, block_end, address, topic0, blockchain, **kwargs)

  > Description: function returns logs data for given block range for specified contract/address

  ** Example needed **

  ### 23: get_block_samples(start_date, samples, blockchain, end_date='latest', utc=0, dates=False)

  > Description: function returns blah blahh blaaahhh

  ** Work needs to be done **

  ### 24: is_archival(endpoint) -> bool

  > Description: function returns if node is an archival node or a full node.



  </details>

- <details><summary><b>Aave</b></summary>

  # Aave

  ## Defined in Aave.py


  ### 1: get_reserves_tokens(pdp_contract, block)

  > Description: function returns reserved tokens for aave protocol v2

  - <details><summary><b>Example</b></summary>

    ```
    from defi_protocols.functions import *

    from defi_protocols import Aave

    f1 = get_contract('0x057835Ad21a177dbdd3090bB1CAE03EaCF78Fc6d', ETHEREUM)

    f2 = Aave.get_reserves_tokens(f1, 'latest')

    print(f2)

    ```

    ```
    output:
    ['0xdAC17F958D2ee523a2206206994597C13D831ec7', '0x2260FAC5E5542a773Aa44fBCfeDf7C193bc2C599', '0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2', '0x0bc529c00C6401aEF6D220BE8C6Ea1667F6Ad93e', '0xE41d2489571d322189246DaFA5ebDe1F4699F498', '0x1f9840a85d5aF5bf1D1762F925BDADdC4201F984', '0x7Fc66500c84A76Ad7e9c93437bFc5Ac33E2DDaE9', '0x0D8775F648430679A709E98d2b0Cb6250d2887EF', '0x4Fabb145d64652a948d72533023f6E7A623C7C53', '0x6B175474E89094C44Da98b954EedeAC495271d0F', '0xF629cBd94d3791C9250152BD8dfBDF380E2a3B9c', '0xdd974D5C2e2928deA5F71b9825b8b646686BD200', '0x514910771AF9Ca656af840dff83E8264EcF986CA', '0x0F5D2fB29fb7d3CFeE444a200298f468908cC942', '0x9f8F72aA9304c8B593d555F12eF6589cC3A579A2', '0x408e41876cCCDC0F92210600ef50372656052a38', '0xC011a73ee8576Fb46F5E1c5751cA3B9Fe0af2a6F', '0x57Ab1ec28D129707052df4dF418D58a2D46d5f51', '0x0000000000085d4780B73119b644AE5ecd22b376', '0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48', '0xD533a949740bb3306d119CC777fa900bA034cd52', '0x056Fd409E1d7A124BD7017459dFEa2F387b6d5Cd', '0xba100000625a3754423978a60c9317c58a424e3D', '0x8798249c2E607446EfB7Ad49eC89dD1865Ff4272', '0xD5147bc8e386d91Cc5DBE72099DAC6C9b99276F5', '0x03ab458634910AaD20eF5f1C8ee96F1D6ac54919', '0xD46bA6D942050d489DBd938a2C909A5d5039A161', '0x8E870D67F660D95d5be530380D0eC0bd388289E1', '0x1494CA1F11D487c2bBe4543E90080AeBa4BA3C2b', '0x853d955aCEf822Db058eb8505911ED77F175b99e', '0x956F47F50A910163D8BF957Cf5846D573E7f87CA', '0xae7ab96520DE3A18E5e111B5EaAb095312D7fE84', '0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72', '0xa693B19d2931d498c5B318dF961919BB4aee87a5', '0x4e3FBD56CD56c3e72c1403e103b45Db9da5B9D2B', '0x111111111117dC0aa78b770fA6A738034120C302', '0x5f98805A4E8be255a32880FDeC7F6728C6568bA0']
    ```
    </details>

  ### 2: get_reserves_tokens_balances(web3, wallet, block, blockchain, decimals=True)

  > Description: function returns reserved token ballances for given wallet

  - <details><summary><b>Example</b></summary>

    ```
    from defi_protocols.functions import *

    from defi_protocols import Aave

    web3 = get_node(ETHEREUM, 'latest', 0)

    f2 = Aave.get_reserves_tokens_balances(web3, '0x849D52316331967b6fF1198e5E32A0eB168D039d', 'latest', ETHEREUM)

    print(f2)

    ```

    ```
    output: [['0x2260FAC5E5542a773Aa44fBCfeDf7C193bc2C599', -25.1759987], ['0xae7ab96520DE3A18E5e111B5EaAb095312D7fE84', 1385.4727732126728]]
    
    ```
    </details>

  ### 3: get_data(wallet, block, blockchain, execution = 1, web3=None, index=0, decimals=True)

  > Description: function returns aave protocol data for given wallet

  - <details><summary><b>Example</b></summary>

    ```
    from defi_protocols.functions import *

    from defi_protocols import Aave

    f3 = Aave.get_data('0x849D52316331967b6fF1198e5E32A0eB168D039d', 'latest', ETHEREUM)

    print(f3)

    ```

    ```
    output: 

    {'collateral_ratio': 422.8517007532872, 'liquidation_ratio': 120.48192771084337, 'eth_price_usd': 1321.28, 'collaterals': [{'token_address': '0xae7ab96520DE3A18E5e111B5EaAb095312D7fE84', 'token_amount': 1385.4727732126728, 'token_price_usd': 1309.82714496}], 'debts': [{'token_address': '0x2260FAC5E5542a773Aa44fBCfeDf7C193bc2C599', 'token_amount': 25.17600199, 'token_price_usd': 17046.574635530906}]}
    
    ```
    </details>


  ### 4: get_all_rewards(wallet, block, blockchain, execution = 1, web3=None, index=0, decimals=True)

  > Description: function returns all the rewards for given wallet from aave protocol

  - <details><summary><b>Example</b></summary>

    ```
    from defi_protocols.functions import *

    from defi_protocols import Aave

    f4 = Aave.get_all_rewards('0x849D52316331967b6fF1198e5E32A0eB168D039d', 'latest', ETHEREUM)

    print(f4)

    ```

    ```
    output: 

    [['0x7Fc66500c84A76Ad7e9c93437bFc5Ac33E2DDaE9', 5.046433045046507]]
    
    ```

  ### 5: underlying(wallet, block, blockchain, execution=1, web3=None, index=0, decimals=True, reward=False)

  > Description: function returns underlying tokens for given wallter from aave protocol

  - <details><summary><b>Example</b></summary>

    ```
    from defi_protocols.functions import *

    from defi_protocols import Aave

    f5 = Aave.underlying('0x849D52316331967b6fF1198e5E32A0eB168D039d', 'latest', ETHEREUM, reward=True)

    print(f5)

    ```

    ```
    output: 

    [[['0x2260FAC5E5542a773Aa44fBCfeDf7C193bc2C599', -25.17600614], ['0xae7ab96520DE3A18E5e111B5EaAb095312D7fE84', 1385.4727732126728]], [['0x7Fc66500c84A76Ad7e9c93437bFc5Ac33E2DDaE9', 5.046433045046507]]]
    
    ```
    
  </details>

## 💙 Contributing

PR's are welcome !

Please open a pull request in dev branch if you want to contribute to this awesome protocols!

Found a Bug ? Create an Issue.


## 💖 Like this project ?

Leave a ⭐ If you think this project is cool.

Follow use on [twitter](https://twitter.com/karpatkey)
