# 🌊 Bot Claim Ocean 🌊

Hello everyone! 👋

Welcome to the SuiOcean Airdrop Bot, an advanced tool designed to help you easily claim Ocean airdrops. As a form of support and also as a referral replacement.

Note: For users who have never tried it, please visit Wave on Sui Bot. For those using my referral, no fee will be charged. 🚀

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

4.  Run with docker command
    ```bash
    sudo docker-compose up -d
    ```
5.  View logs
    ```bash
    docker logs --follow bot-claim-ocean-app-1
    ```

Good luck! If you have any questions or issues, feel free to contact me. Thank you for using the SuiOcean Airdrop Claim Bot. 🚀
