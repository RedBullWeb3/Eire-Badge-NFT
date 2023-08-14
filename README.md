# Eire Harvest NFT minting dapp 🔥

https://eire.vercel.app/

![Kristof_female_irish_NFT_sticker_in_the_cartoon_celtic_art_colo_676b5041-e5bd-45ca-9f8f-2d5c6a170d15](https://github.com/RedBullWeb3/Eire-Badge-NFT/assets/65456462/2f56d700-4774-48be-8c63-e5f5be07235d)


Alpha:
![Zrzut ekranu 2023-07-27 145245](https://github.com/RedBullWeb3/Eire-Badge-NFT/assets/65456462/23817f8e-b48e-4ad2-a116-2d1f05d281aa)


Beta:
![Zrzut ekranu 2023-08-14 140544](https://github.com/RedBullWeb3/Eire-Badge-NFT/assets/65456462/962144da-0972-481d-97f4-1ff1c842ec16)




This repo provides a nice and easy way for linking an created NFT smart contract to this minting dapp. There are two ways of using this repo, you can go the simple route or the more complex one.

The simple route is so simple, all you need to do is download the build folder on the release page and change the configuration to fit your needs. (Follow the video for a walk through).

The more complex route allows you to add additional functionality if you are comfortable with coding in react.js. (Follow the below instructions for a walk through).

## Installation 🛠️

If you are cloning the project then run this first, otherwise you can download the source code on the release page and skip this step.

```sh
https://github.com/RedBullWeb3/Eire-Badge-NFT/tree/main
```

Make sure you have node.js installed so you can use npm, then run:

```sh
npm install
```

## Usage ℹ️

In order to make use of this dapp, all you need to do is change the configurations to point to your smart contract as well as update the images and theme file.

For the most part all the changes will be in the `public` folder.

To link up your existing smart contract, go to the `public/config/config.json` file and update the following fields to fit your smart contract, network and marketplace details. The cost field should be in wei.

Note: this dapp is designed to work with the intended NFT smart contract, that only takes one parameter in the mint function "mintAmount". But you can change that in the App.js file if you need to use a smart contract that takes 2 params.

```json
{
  "CONTRACT_ADDRESS": "0xe716f72d6c43bfb1a876d9843216bcc9019d8e9e",
  "SCAN_LINK": "https://explorer.linea.build/token/0xE716F72D6c43bfb1A876d9843216bCC9019d8E9e/token-transfers",
  "NETWORK": {
    "NAME": "Linea",
    "SYMBOL": "ETH",
    "ID": 59144
  },
  "NFT_NAME": "Eire Harvest",
  "SYMBOL": "EHH",
  "MAX_SUPPLY": 431,
  "WEI_COST": 100000000000000,
  "DISPLAY_COST": 0.0001,
  "GAS_LIMIT": 28500000,
  "MARKETPLACE": "eIRE Zk",
  "MARKETPLACE_LINK": "https://omnisea.org/hqJXPqnPjdl9R2PBef1V",
  "SHOW_BACKGROUND": true
}
```

Make sure you copy the contract ABI from remix and paste it in the `public/config/abi.json` file.
(follow the youtube video if you struggle with this part).

Now you will need to create and change 2 images and a gif in the `public/config/images` folder, `bg.png`, `example.gif` and `logo.png`.

Next change the theme colors to your liking in the `public/config/theme.css` file.

```css
:root {
  --primary: #ebc908;
  --primary-text: #1a1a1a;
  --secondary: #ff1dec;
  --secondary-text: #ffffff;
  --accent: #ffffff;
  --accent-text: #000000;
}
```

Now you will need to create and change the `public/favicon.ico`, `public/logo192.png`, and
`public/logo512.png` to your brand images.

Remember to update the title and description the `public/index.html` file

```html
<title>Eire Harvest</title>
<meta name="description" content="Mint your EireHarvest NFT" />
```

Also remember to update the short_name and name fields in the `public/manifest.json` file

```json
{
  "short_name": "EHH",
  "name": "Eire Harvest"
}
```

After all the changes you can run.

```sh
npm run start
```

Or create the build if you are ready to deploy.

```sh
npm run build
```

Now you can host the contents of the build folder on a server.

That's it! you're done.
