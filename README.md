# 🌊 Bot Claim Ocean 🌊

Hello everyone! 👋

Welcome to the Bot Claim Ocean, an advanced tool designed to help you easily claim Ocean airdrops. For each claim process i will take fee 0.0003 SUI.
This Bot will auto Claim Ocean -> auto adding SUI to ref Wallet for GAS fee -> auto transfer Ocean from ref wallet to main wallet

Note: For users who have never tried it, please visit [Wave on Sui Bot](t.me/waveonsuibot/walletapp?startapp=3831437). For those using my referral, no fee will be charged. 🚀

## Installation Steps:

Follow the steps below to install and run this bot on your system:

1.  **Install Docker:** Make sure Node.js is installed on your computer. If not, please follow step bellow:

    a. First, update your existing list of packages:

    ```bash
    sudo apt update
    ```

    b. Next, install a few prerequisite packages which let apt use packages over HTTPS:

    ```bash
    sudo apt install apt-transport-https ca-certificates curl software-properties-common
    ```

    c. Then add the GPG key for the official Docker repository to your system:

    ```bash
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    ```

    d. Add the Docker repository to APT sources:

    ```bash
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
    ```

    e. This will also update our package database with the Docker packages from the newly added repo.

    ```bash
    apt-cache policy docker-ce
    ```

    f. Finally, install Docker:

    ```bash
    sudo apt install docker-ce
    ```

2.  **Clone this repository:**

    ```bash
      git clone https://github.com/phuongpd2k/bot-claim-ocean.git $HOME/bot-claim-ocean && cd $HOME/bot-claim-ocean
    ```

3.  Change file config.json

    ```json
    {
      "sendFee": false, // If set true: auto send 0.1 SUI from main wallet to ref wallet if ref have SUI lower than 0.1
      "mainPhrase": "phr1 phr2 phr3 ... ...", // phrases for main wallet
      "refPhrases": ["kata1 kata2 kata3 ... ...", "hira1 hira2 hira3 ... ..."] // phrases for ref wallet
    }
    ```

    ### Definition of fields:

    a. sendFee: 
    - if TRUE:  Automatically send GAS fee from MAIN wallet to REF wallets if REF wallet has less than 0.01 SUI
    - if FALSE: do nothing
    
    b. mainPhrases: seed phrases of the MAIN wallet (the wallet you want to focus all OCEAN on because REF wallets with 20 OCEAN or more will be sent to the MAIN wallet
    
    c. refPhrases: seed phrases of ref wallets, declared in array form



4.  Run with docker command
    ```bash
    sudo docker-compose up -d
    ```
5.  View logs
    ```bash
    docker logs --follow bot-claim-ocean-app-1
    ```

Good luck! If you have any questions or issues, feel free to contact me. Thank you for using the Ocean Claim Bot. 🚀
