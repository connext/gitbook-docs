# Deployments

## Contract Deployments

A full list of deployed contracts can be found in the [deployments.json](https://github.com/connext/monorepo/blob/main/packages/deployments/contracts/deployments.json) file. This contains deployments for all environments and is difficult to parse through manually. You should only need to reference it for automation or as a source of truth. For convenience, we extracted the important contract addresses and listed them here.

## Mainnet Contracts

### Ethereum

> Domain ID: 6648936

> Chain ID: 1

| Core Contract                                                                                    | Address                                    |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------ |
| [Connext](https://louper.dev/diamond/0x8898B472C54c31894e3B9bb83cEA802a5d0e63C6?network=mainnet) | 0x8898B472C54c31894e3B9bb83cEA802a5d0e63C6 |

| Asset Contract                                                                  | Address                                    | Flavor    |
| ------------------------------------------------------------------------------- | ------------------------------------------ | --------- |
| [NEXT](https://etherscan.io/token/0xFE67A4450907459c3e1FFf623aA927dD4e28c67a)   | 0xFE67A4450907459c3e1FFf623aA927dD4e28c67a | Canonical |
| [USDC](https://etherscan.io/address/0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48) | 0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48 | Canonical |
| [WETH](https://etherscan.io/address/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2) | 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2 | Canonical |
| [DAI](https://etherscan.io/address/0x6b175474e89094c44da98b954eedeac495271d0f)  | 0x6B175474E89094C44Da98b954EedeAC495271d0F | Canonical |
| [USDT](https://etherscan.io/address/0xdac17f958d2ee523a2206206994597c13d831ec7) | 0xdAC17F958D2ee523a2206206994597C13D831ec7 | Canonical |

| Peripheral Contract                                                                  | Address                                    | Description    |
| ------------------------------------------------------------------------------------ | ------------------------------------------ | -------------- |
| [Unwrapper](https://etherscan.io/address/0x268682b7D9992aE7e2ca4A8bCc9D9655FB06056F) | 0x268682b7D9992aE7e2ca4A8bCc9D9655FB06056F | WETH Unwrapper |

### Optimism

> Domain ID: 1869640809

> Chain ID: 10

| Core Contract                                                                                     | Address                                    |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| [Connext](https://louper.dev/diamond/0x8f7492DE823025b4CfaAB1D34c58963F2af5DEDA?network=optimism) | 0x8f7492DE823025b4CfaAB1D34c58963F2af5DEDA |

| Asset Contract                                                                                  | Address                                    | Flavor        |
| ----------------------------------------------------------------------------------------------- | ------------------------------------------ | ------------- |
| [NEXT](https://optimistic.etherscan.io/address/0x58b9cB810A68a7f3e1E4f8Cb45D1B9B3c79705E8#code) | 0x58b9cB810A68a7f3e1E4f8Cb45D1B9B3c79705E8 | Local/Adopted |
| [nextUSDC](https://optimistic.etherscan.io/address/0x67E51f46e8e14D4E4cab9dF48c59ad8F512486DD)  | 0x67E51f46e8e14D4E4cab9dF48c59ad8F512486DD | Local         |
| [USDC](https://optimistic.etherscan.io/address/0x7F5c764cBc14f9669B88837ca1490cCa17c31607)      | 0x7F5c764cBc14f9669B88837ca1490cCa17c31607 | Adopted       |
| [nextWETH](https://optimistic.etherscan.io/address/0xbAD5B3c68F855EaEcE68203312Fd88AD3D365e50)  | 0xbAD5B3c68F855EaEcE68203312Fd88AD3D365e50 | Local         |
| [WETH](https://optimistic.etherscan.io/address/0x4200000000000000000000000000000000000006)      | 0x4200000000000000000000000000000000000006 | Adopted       |
| [nextDAI](https://optimistic.etherscan.io/address/0xd64Bd028b560bbFc732eA18f282c64B86F3468e0)   | 0xd64Bd028b560bbFc732eA18f282c64B86F3468e0 | Local         |
| [DAI](https://optimistic.etherscan.io/address/0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1)       | 0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1 | Adopted       |
| [nextUSDT](https://optimistic.etherscan.io/address/0x4cBB28FA12264cD8E87C62F4E1d9f5955Ce67D20)  | 0x4cBB28FA12264cD8E87C62F4E1d9f5955Ce67D20 | Local         |
| [USDT](https://optimistic.etherscan.io/address/0x94b008aA00579c1307B0EF2c499aD98a8ce58e58)      | 0x94b008aA00579c1307B0EF2c499aD98a8ce58e58 | Adopted       |

| Peripheral Contract                                                                             | Address                                    | Description    |
| ----------------------------------------------------------------------------------------------- | ------------------------------------------ | -------------- |
| [Unwrapper](https://optimistic.etherscan.io/address/0x7Fe09d217d646a6213e51b237670Bc326188cB93) | 0x7Fe09d217d646a6213e51b237670Bc326188cB93 | WETH Unwrapper |

### Polygon

> Domain ID: 1886350457

> Chain ID: 137

| Core Contract                                                                                    | Address                                    |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------ |
| [Connext](https://louper.dev/diamond/0x11984dc4465481512eb5b777E44061C158CF2259?network=polygon) | 0x11984dc4465481512eb5b777E44061C158CF2259 |

| Asset Contract                                                                         | Address                                    | Flavor        |
| -------------------------------------------------------------------------------------- | ------------------------------------------ | ------------- |
| [NEXT](https://polygonscan.com/address/0x58b9cB810A68a7f3e1E4f8Cb45D1B9B3c79705E8)     | 0x58b9cB810A68a7f3e1E4f8Cb45D1B9B3c79705E8 | Local/Adopted |
| [nextUSDC](https://polygonscan.com/address/0xF96C6d2537e1af1a9503852eB2A4AF264272a5B6) | 0xF96C6d2537e1af1a9503852eB2A4AF264272a5B6 | Local         |
| [USDC](https://polygonscan.com/address/0x2791Bca1f2de4661ED88A30C99A7a9449Aa84174)     | 0x2791Bca1f2de4661ED88A30C99A7a9449Aa84174 | Adopted       |
| [nextWETH](https://polygonscan.com/address/0x4b8BaC8Dd1CAA52E32C07755c17eFadeD6A0bbD0) | 0x4b8BaC8Dd1CAA52E32C07755c17eFadeD6A0bbD0 | Local         |
| [WETH](https://polygonscan.com/address/0x7ceB23fD6bC0adD59E62ac25578270cFf1b9f619)     | 0x7ceB23fD6bC0adD59E62ac25578270cFf1b9f619 | Adopted       |
| [nextDAI](https://polygonscan.com/address/0xaDCe87b14d570665222C1172D18a221BF7690d5a)  | 0xaDCe87b14d570665222C1172D18a221BF7690d5a | Local         |
| [DAI](https://polygonscan.com/address/0x8f3Cf7ad23Cd3CaDbD9735AFf958023239c6A063)      | 0x8f3Cf7ad23Cd3CaDbD9735AFf958023239c6A063 | Adopted       |
| [nextUSDT](https://polygonscan.com/address/0xE221C5A2a8348f12dcb2b0e88693522EbAD2690f) | 0xE221C5A2a8348f12dcb2b0e88693522EbAD2690f | Local         |
| [USDT](https://polygonscan.com/address/0xc2132D05D31c914a87C6611C10748AEb04B58e8F)     | 0xc2132D05D31c914a87C6611C10748AEb04B58e8F | Adopted       |

| Peripheral Contract                                                                     | Address                                    | Description    |
| --------------------------------------------------------------------------------------- | ------------------------------------------ | -------------- |
| [Unwrapper](https://polygonscan.com/address/0x7E8F8B2dA3dc5Ad9c9Dfd1A832331A039d4f3f74) | 0x7E8F8B2dA3dc5Ad9c9Dfd1A832331A039d4f3f74 | WETH Unwrapper |

### Arbitrum One

> Domain ID: 1634886255

> Chain ID: 42161

| Core Contract                                                                                     | Address                                    |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| [Connext](https://louper.dev/diamond/0xEE9deC2712cCE65174B561151701Bf54b99C24C8?network=arbitrum) | 0xEE9deC2712cCE65174B561151701Bf54b99C24C8 |

| Asset Contract                                                                     | Address                                    | Flavor        |
| ---------------------------------------------------------------------------------- | ------------------------------------------ | ------------- |
| [NEXT](https://arbiscan.io/address/0x58b9cB810A68a7f3e1E4f8Cb45D1B9B3c79705E8)     | 0x58b9cB810A68a7f3e1E4f8Cb45D1B9B3c79705E8 | Local/Adopted |
| [nextUSDC](https://arbiscan.io/address/0x8c556cF37faa0eeDAC7aE665f1Bb0FbD4b2eae36) | 0x8c556cF37faa0eeDAC7aE665f1Bb0FbD4b2eae36 | Local         |
| [USDC](https://arbiscan.io/address/0xFF970A61A04b1cA14834A43f5dE4533eBDDB5CC8)     | 0xFF970A61A04b1cA14834A43f5dE4533eBDDB5CC8 | Adopted       |
| [nextWETH](https://arbiscan.io/address/0x2983bf5c334743Aa6657AD70A55041d720d225dB) | 0x2983bf5c334743Aa6657AD70A55041d720d225dB | Local         |
| [WETH](https://arbiscan.io/address/0x82aF49447D8a07e3bd95BD0d56f35241523fBab1)     | 0x82aF49447D8a07e3bd95BD0d56f35241523fBab1 | Adopted       |
| [nextDAI](https://arbiscan.io/address/0xfDe99b3B3fbB69553D7DaE105EF34Ba4FE971190)  | 0xfDe99b3B3fbB69553D7DaE105EF34Ba4FE971190 | Local         |
| [DAI](https://arbiscan.io/address/0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1)      | 0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1 | Adopted       |
| [nextUSDT](https://arbiscan.io/address/0x2fD7E61033b3904c65AA9A9B83DCd344Fa19Ffd2) | 0x2fD7E61033b3904c65AA9A9B83DCd344Fa19Ffd2 | Local         |
| [USDT](https://arbiscan.io/address/0xFd086bC7CD5C481DCC9C85ebE478A1C0b69FCbb9)     | 0xFd086bC7CD5C481DCC9C85ebE478A1C0b69FCbb9 | Adopted       |

| Peripheral Contract                                                                 | Address                                    | Description    |
| ----------------------------------------------------------------------------------- | ------------------------------------------ | -------------- |
| [Unwrapper](https://arbiscan.io/address/0x429b9eb01362b2799131EfCC44319689b662999D) | 0x429b9eb01362b2799131EfCC44319689b662999D | WETH Unwrapper |

### Binance Smart Chain

> Domain ID: 6450786

> Chain ID: 56

| Core Contract                                                                                    | Address                                    |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------ |
| [Connext](https://louper.dev/diamond/0xCd401c10afa37d641d2F594852DA94C700e4F2CE?network=binance) | 0xCd401c10afa37d641d2F594852DA94C700e4F2CE |

| Asset Contract                                                                     | Address                                    | Flavor        |
| ---------------------------------------------------------------------------------- | ------------------------------------------ | ------------- |
| [NEXT](https://bscscan.com/address/0x58b9cB810A68a7f3e1E4f8Cb45D1B9B3c79705E8)     | 0x58b9cB810A68a7f3e1E4f8Cb45D1B9B3c79705E8 | Local/Adopted |
| [nextUSDC](https://bscscan.com/address/0x5e7D83dA751F4C9694b13aF351B30aC108f32C38) | 0x5e7D83dA751F4C9694b13aF351B30aC108f32C38 | Local         |
| [USDC](https://bscscan.com/address/0x8AC76a51cc950d9822D68b83fE1Ad97B32Cd580d)     | 0x8AC76a51cc950d9822D68b83fE1Ad97B32Cd580d | Adopted       |
| [nextWETH](https://bscscan.com/address/0xA9CB51C666D2AF451d87442Be50747B31BB7d805) | 0xA9CB51C666D2AF451d87442Be50747B31BB7d805 | Local         |
| [WETH](https://bscscan.com/address/0x2170Ed0880ac9A755fd29B2688956BD959F933F8)     | 0x2170Ed0880ac9A755fd29B2688956BD959F933F8 | Adopted       |
| [nextDAI](https://bscscan.com/address/0x86a343BCF17D79C475d300eed35F0145F137D0c9)  | 0x86a343BCF17D79C475d300eed35F0145F137D0c9 | Local         |
| [DAI](https://bscscan.com/address/0x1AF3F329e8BE154074D8769D1FFa4eE058B1DBc3)      | 0x1AF3F329e8BE154074D8769D1FFa4eE058B1DBc3 | Adopted       |
| [nextUSDT](https://bscscan.com/address/0xD609f26B5547d5E31562B29150769Cb7c774B97a) | 0xD609f26B5547d5E31562B29150769Cb7c774B97a | Local         |
| [USDT](https://bscscan.com/address/0x55d398326f99059fF775485246999027B3197955)     | 0x55d398326f99059fF775485246999027B3197955 | Adopted       |

| Peripheral Contract                                                                 | Address                                    | Description    |
| ----------------------------------------------------------------------------------- | ------------------------------------------ | -------------- |
| [Unwrapper](https://bscscan.com/address/0x2c7B8c1a13F2a7854B9299E4d22809A8B1E05De5) | 0x2c7B8c1a13F2a7854B9299E4d22809A8B1E05De5 | WETH Unwrapper |

### Gnosis

> Domain ID: 6778479

> Chain ID: 100

| Core Contract                                                                                 | Address                                    |
| --------------------------------------------------------------------------------------------- | ------------------------------------------ |
| [Connext](https://louper.dev/diamond/0x5bB83e95f63217CDa6aE3D181BA580Ef377D2109?network=xdai) | 0x5bB83e95f63217CDa6aE3D181BA580Ef377D2109 |

| Asset Contract                                                                       | Address                                    | Flavor        |
| ------------------------------------------------------------------------------------ | ------------------------------------------ | ------------- |
| [NEXT](https://gnosisscan.io/address/0x58b9cb810a68a7f3e1e4f8cb45d1b9b3c79705e8)     | 0x58b9cB810A68a7f3e1E4f8Cb45D1B9B3c79705E8 | Local/Adopted |
| [nextUSDC](https://gnosisscan.io/address/0x44CF74238d840a5fEBB0eAa089D05b763B73faB8) | 0x44CF74238d840a5fEBB0eAa089D05b763B73faB8 | Local         |
| [USDC](https://gnosisscan.io/address/0xDDAfbb505ad214D7b80b1f830fcCc89B60fb7A83)     | 0xDDAfbb505ad214D7b80b1f830fcCc89B60fb7A83 | Adopted       |
| [nextWETH](https://gnosisscan.io/address/0x538E2dDbfDf476D24cCb1477A518A82C9EA81326) | 0x538E2dDbfDf476D24cCb1477A518A82C9EA81326 | Local         |
| [WETH](https://gnosisscan.io/address/0x6A023CCd1ff6F2045C3309768eAd9E68F978f6e1)     | 0x6A023CCd1ff6F2045C3309768eAd9E68F978f6e1 | Adopted       |
| [nextDAI](https://gnosisscan.io/address/0x0e1D5Bcd2Ac5CF2f71841A9667afC1E995CaAf4F)  | 0x0e1D5Bcd2Ac5CF2f71841A9667afC1E995CaAf4F | Local         |
| [DAI](https://gnosisscan.io/address/0xe91D153E0b41518A2Ce8Dd3D7944Fa863463a97d)      | 0xe91D153E0b41518A2Ce8Dd3D7944Fa863463a97d | Adopted       |
| [nextUSDT](https://gnosisscan.io/address/0xF4d944883D6FddC56d3534986feF82105CaDbfA1) | 0xF4d944883D6FddC56d3534986feF82105CaDbfA1 | Local         |
| [USDT](https://gnosisscan.io/address/0x4ECaBa5870353805a9F068101A40E0f32ed605C6)     | 0x4ECaBa5870353805a9F068101A40E0f32ed605C6 | Adopted       |

| Peripheral Contract                                                                   | Address                                    | Description    |
| ------------------------------------------------------------------------------------- | ------------------------------------------ | -------------- |
| [Unwrapper](https://gnosisscan.io/address/0x642c27a96dFFB6f21443A89b789a3194Ff8399fa) | 0x642c27a96dFFB6f21443A89b789a3194Ff8399fa | WETH Unwrapper |

### Linea

> Domain ID: 1818848877

> Chain ID: 59144

| Core Contract                                                                         | Address                                    |
| ------------------------------------------------------------------------------------- | ------------------------------------------ |
| [Connext](https://lineascan.build/address/0xa05eF29e9aC8C75c530c2795Fa6A800e188dE0a9) | 0xa05eF29e9aC8C75c530c2795Fa6A800e188dE0a9 |

<table><thead><tr><th>Asset Contract</th><th width="251.33333333333331">Address</th><th>Flavor</th></tr></thead><tbody><tr><td><a href="https://lineascan.build/address/0x331152ca43B50B39F3a9f203685B98dbb9b42342">nextUSDC</a></td><td>0x331152ca43B50B39F3a9f203685B98dbb9b42342</td><td>Local</td></tr><tr><td><a href="https://lineascan.build/address/0x176211869cA2b568f2A7D4EE941E073a821EE1ff">USDC</a></td><td>0x176211869cA2b568f2A7D4EE941E073a821EE1ff</td><td>Adopted</td></tr><tr><td><a href="https://lineascan.build/address/0x0573AD07cA4f74757e5B2417Bf225BEbeBcF66D9">nextWETH</a></td><td>0x0573AD07cA4f74757e5B2417Bf225BEbeBcF66D9</td><td>Local</td></tr><tr><td><a href="https://lineascan.build/address/0xe5D7C2a44FfDDf6b295A15c148167daaAf5Cf34f">WETH</a></td><td>0xe5D7C2a44FfDDf6b295A15c148167daaAf5Cf34f</td><td>Adopted</td></tr><tr><td><a href="https://lineascan.build/address/0x7360a597290612787833EE924C449C61Cc0689E4">nextDAI</a></td><td>0x7360a597290612787833EE924C449C61Cc0689E4</td><td>Local</td></tr><tr><td><a href="https://lineascan.build/address/0x4AF15ec2A0BD43Db75dd04E62FAA3B8EF36b00d5">DAI</a></td><td>0x4AF15ec2A0BD43Db75dd04E62FAA3B8EF36b00d5</td><td>Adopted</td></tr><tr><td><a href="https://lineascan.build/address/0xbD7eAEd30936670C931B718F5D9014AFf82fC767">nextUSDT</a></td><td>0xbD7eAEd30936670C931B718F5D9014AFf82fC767</td><td>Local</td></tr><tr><td><a href="https://lineascan.build/address/0xA219439258ca9da29E9Cc4cE5596924745e12B93">USDT</a></td><td>0xA219439258ca9da29E9Cc4cE5596924745e12B93</td><td>Adopted</td></tr></tbody></table>

| Peripheral Contract                                                                     | Address                                    | Description    |
| --------------------------------------------------------------------------------------- | ------------------------------------------ | -------------- |
| [Unwrapper](https://lineascan.build/address/0x5A53576DDE5071719a9A3a9E78e68cbcDf863253) | 0x5A53576DDE5071719a9A3a9E78e68cbcDf863253 | WETH Unwrapper |

### Base

> Domain ID: 1650553709

> Chain ID: 8453

| Core Contract                                                                      | Address                                    |
| ---------------------------------------------------------------------------------- | ------------------------------------------ |
| [Connext](https://basescan.org/address/0xB8448C6f7f7887D36DcA487370778e419e9ebE3F) | 0xB8448C6f7f7887D36DcA487370778e419e9ebE3F |

<table><thead><tr><th>Asset Contract</th><th width="261.3333333333333">Address</th><th>Flavor</th></tr></thead><tbody><tr><td><a href="https://basescan.org/address/0xE08D4907b2C7aa5458aC86596b6D17B1feA03F7E">nextWETH</a></td><td>0xE08D4907b2C7aa5458aC86596b6D17B1feA03F7E</td><td>Local</td></tr><tr><td><a href="https://basescan.org/address/0x4200000000000000000000000000000000000006">WETH</a></td><td>0x4200000000000000000000000000000000000006</td><td>Adopted</td></tr><tr><td><a href="https://basescan.org/address/0xC90a82e926d3a87899b3717aba0262BF66Ef53E8">nextDAI</a></td><td>0xC90a82e926d3a87899b3717aba0262BF66Ef53E8</td><td>Local</td></tr><tr><td><a href="https://basescan.org/address/0x50c5725949A6F0c72E6C4a641F24049A917DB0Cb">DAI</a></td><td>0x50c5725949A6F0c72E6C4a641F24049A917DB0Cb</td><td>Adopted</td></tr><tr><td><a href="https://basescan.org/address/0x1ede59e0d39B14c038698B1036BDE9a4819C86D4">nextUSDC</a></td><td>0x1ede59e0d39B14c038698B1036BDE9a4819C86D4</td><td>Local</td></tr><tr><td><a href="https://basescan.org/address/0x833589fcd6edb6e08f4c7c32d4f71b54bda02913">USDC</a></td><td>0x833589fcd6edb6e08f4c7c32d4f71b54bda02913</td><td>Adopted</td></tr></tbody></table>

<table><thead><tr><th>Peripheral Contract</th><th width="254.33333333333331">Address</th><th>Description</th></tr></thead><tbody><tr><td><a href="https://basescan.org/address/0x01EdE4Fdf8CF7Ef9942a935305C3145f8dAa180A">Unwrapper</a></td><td>0x01EdE4Fdf8CF7Ef9942a935305C3145f8dAa180A</td><td>WETH Unwrapper</td></tr></tbody></table>

### Metis

> Domain ID: 1835365481

> Chain ID: 1088

| Core Contract                                                                                     | Address                                    |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| [Connext](https://andromeda-explorer.metis.io/address/0x6B142227A277CE62808E0Df93202483547Ec0188) | 0x6B142227A277CE62808E0Df93202483547Ec0188 |

<table><thead><tr><th>Asset Contract</th><th width="261.3333333333333">Address</th><th>Flavor</th></tr></thead><tbody><tr><td><a href="https://andromeda-explorer.metis.io/address/0x3883B5Bdd61BA1b687de69eE50c9738D5ec501E9">nextWETH</a></td><td>0x3883B5Bdd61BA1b687de69eE50c9738D5ec501E9</td><td>Local</td></tr><tr><td><a href="https://andromeda-explorer.metis.io/address/0x420000000000000000000000000000000000000A">WETH</a></td><td>0x420000000000000000000000000000000000000a</td><td>Adopted</td></tr><tr><td><a href="https://andromeda-explorer.metis.io/address/0xa6A8d22D5da43C9f6E5cF7b4e50941784e70F688">nextUSDT</a></td><td>0xa6A8d22D5da43C9f6E5cF7b4e50941784e70F688</td><td>Local</td></tr><tr><td><a href="https://andromeda-explorer.metis.io/address/0xbB06DCA3AE6887fAbF931640f67cab3e3a16F4dC">USDT</a></td><td>0xbB06DCA3AE6887fAbF931640f67cab3e3a16F4dC</td><td>Adopted</td></tr><tr><td><a href="https://andromeda-explorer.metis.io/address/0x9ac9aD5A82Ccd0Ab7584a037A7A2334Dc3715Be2">nextUSDC</a></td><td>0x9ac9aD5A82Ccd0Ab7584a037A7A2334Dc3715Be2</td><td>Local</td></tr><tr><td><a href="https://andromeda-explorer.metis.io/address/0xEA32A96608495e54156Ae48931A7c20f0dcc1a21">USDC</a></td><td>0xEA32A96608495e54156Ae48931A7c20f0dcc1a21</td><td>Adopted</td></tr></tbody></table>

<table><thead><tr><th>Peripheral Contract</th><th width="254.33333333333331">Address</th><th>Description</th></tr></thead><tbody><tr><td><a href="https://andromeda-explorer.metis.io/address/0x8Ef3E1300857FDF616dfE2fcBced4ac6a61Fe774">Unwrapper</a></td><td>0x8Ef3E1300857FDF616dfE2fcBced4ac6a61Fe774</td><td>WETH Unwrapper</td></tr></tbody></table>

### Mode

> Domain ID: 1836016741

> Chain ID: 34443

| Core Contract                                                                               | Address                                    |
| ------------------------------------------------------------------------------------------- | ------------------------------------------ |
| [Connext](https://explorer.mode.network/address/0x7380511493DD4c2f1dD75E9CCe5bD52C787D4B51) | 0x7380511493DD4c2f1dD75E9CCe5bD52C787D4B51 |

<table><thead><tr><th>Asset Contract</th><th width="261.3333333333333">Address</th><th>Flavor</th></tr></thead><tbody><tr><td><a href="https://explorer.mode.network/address/0x609aEfb9FB2Ee8f2FDAd5dc48efb8fA4EE0e80fB">nextWETH</a></td><td>0x609aEfb9FB2Ee8f2FDAd5dc48efb8fA4EE0e80fB</td><td>Local</td></tr><tr><td><a href="https://explorer.mode.network/address/0x4200000000000000000000000000000000000006">WETH</a></td><td>0x4200000000000000000000000000000000000006</td><td>Adopted</td></tr></tbody></table>

<table><thead><tr><th>Peripheral Contract</th><th width="254.33333333333331">Address</th><th>Description</th></tr></thead><tbody><tr><td><a href="https://explorer.mode.network/address/0x2c8DA9c3166085acebc70Ad9491cA2bfa10C8b9F">Unwrapper</a></td><td>0x2c8DA9c3166085acebc70Ad9491cA2bfa10C8b9F</td><td>WETH Unwrapper</td></tr></tbody></table>

## Testnet Contracts

Note that the Test Token is a mintable ERC20. The open `mint` function has the signature `mint(address account, uint256 amount)` and can be freely called.

### Sepolia

> Domain ID: 1936027759

> Chain ID: 11155111

| Core Contract | Address                                    |
| ------------- | ------------------------------------------ |
| Connext       | 0x445fbf9cCbaf7d557fd771d56937E94397f43965 |

| Asset Contract | Address                                    | Flavor    |
| -------------- | ------------------------------------------ | --------- |
| TEST           | 0xd26e3540A0A368845B234736A0700E0a5A821bBA | Canonical |

### Optimism-Sepolia

> Domain ID: 1869640549

> Chain ID: 11155420

| Core Contract | Address                                    |
| ------------- | ------------------------------------------ |
| Connext       | 0x8247ed6d0a344eeae4edBC7e44572F1B70ECA82A |

| Asset Contract | Address                                    | Flavor    |
| -------------- | ------------------------------------------ | --------- |
| TEST           | 0x7Fa13D6CB44164ea09dF8BCc673A8849092D435b | Canonical |

### Arbitrum-Sepolia

> Domain ID: 1633842021

> Chain ID: 421614

| Core Contract | Address                                    |
| ------------- | ------------------------------------------ |
| Connext       | 0x1780Ac087Cbe84CA8feb75C0Fb61878971175eb8 |

| Asset Contract | Address                                    | Flavor    |
| -------------- | ------------------------------------------ | --------- |
| TEST           | 0xaBF282c88DeD3e386701a322e76456c062468Ac2 | Canonical |

### X1-Testnet

> Domain ID: 2016506996

> Chain ID: 195

| Core Contract | Address                                    |
| ------------- | ------------------------------------------ |
| Connext       | 0xDB8310cAa57B052ab270A573B512dc5644558f0A |

| Asset Contract | Address                                    | Flavor    |
| -------------- | ------------------------------------------ | --------- |
| TEST           | 0x471F702E7D96E541488140042bCD1206Ae55CCa5 | Canonical |

## User Interfaces

### Bridge UI

A bridge UI where users can transfer assets across domains. Here you can also mint `TEST` tokens with the faucet.

[https://amarok-testnet.coinhippo.io](https://amarok-testnet.coinhippo.io)

### Connextscan

This is the testnet scanner site where you can track the status of transfers by `transferId`.

[https://testnet.amarok.connextscan.io](https://testnet.amarok.connextscan.io)
