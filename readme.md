Les contrats devront être fait en solidity 0.8 et les script en js ou ts avec web3 ou ethers.js

- Fork UniswapV2 (4 pts)
    - Contrats : 
        - Faire un 1er commit où les contrats d’uniswap seront renommé: XYSwapFactory, XYSwapPair, XYSwapRouter où X et Y sont vos initial 
            - https://github.com/Uniswap/v2-core pour la factory et la pair
            - https://github.com/Uniswap/v2-periphery pour le router 
        - 3 tokens mintable sans restriction: fUSDC, fUSDT et fDAI 
        - Fork du contrat WETH (https://etherscan.io/address/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2#code)

    - Script : 
        - Création d’une pair pour chaque token: fUSDC/WETH, fUSDT/WETH et fDAI/WETH
        - Ajout de liquidité dans les 3 pairs
        - Effectuer un swap via le router
        
        
- Fork Masterchef Sushiswap (3 pts):
    - Contrat : 
        - Création d’un ERC20 mintable XYS (XY étant vos initials) qui peut être minter uniquement par le contrat Masterchef et le contrat de stacking 
        - Fork du contrat Masterchef (https://github.com/sushiswap/sushiswap/blob/canary/contracts/MasterChef.sol)

    - Script
        - Ajout des récompenses sur fUSDC/WETH (30%), fUSDT/WETH (20%) et fDAI/WETH (50%) avec le nombre de rewards par block choisie a 
           votre convenance
           
- Stacking (3 pts)
    - Contrat
        - Stake ses XYS contre des stkXYS où les stkXYS représente des shares du montant total détenue par le contrat
        - Unstake ses stkXYS contre des XYS et récupérer le montant correspondant aux shares
        - Function exécutable toutes les heures qui mint des tokens XYS dans ce contrat
        vous pouvez vous inspirez des vaults de yearn pour cela: https://github.com/yearn/yearn-protocol/blob/develop/contracts/vaults/yDelegatedVault.sol  

- WebUI (2 pts bonus)
    - Faire une interface web avec les fonctionnalités des différents contrat

