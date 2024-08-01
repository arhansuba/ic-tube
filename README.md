# IC-Tube
IC-Tube is a decentralized video streaming platform built on ICP Chain Fusion, utilizing Livepeer for video processing and IPFS for content storage. It allows users to upload, view, and manage video content in a decentralized manner, with integration for blockchain-based features.

Table of Contents
Introduction
Features
Project Structure
Installation
Usage
Configuration
Contracts
Subgraph
Scripts
Contributing
License
Introduction
IC-Tube is designed to provide a decentralized solution for video streaming and management. It integrates with Livepeer for video encoding and streaming and uses IPFS for storing video content. The platform supports features such as video uploading, playback, and theming.

Features
Decentralized Video Uploads: Upload and manage videos using IPFS.
Video Playback: Stream videos with Livepeer integration.
Customizable Themes: Support for theme toggling to customize the user interface.
GraphQL Subgraph: Provides a subgraph for querying video data.
Project Structure
css
Kodu kopyala
ic-tube/
├── .devcontainer/
├── canisters/
│   └── chain_fusion/
├── src/
│   ├── Cargo.toml
│   └── chain_fusion.did
├── contracts/
│   └── IcTube.sol
├── frontend/
│   ├── clients/
│   │   ├── apollo.ts
│   │   ├── index.ts
│   │   └── livepeer.ts
│   ├── components/
│   │   ├── upload/
│   │   │   ├── VideoInput.tsx
│   │   │   ├── Background.tsx
│   │   │   ├── Player.tsx
│   │   │   ├── ThemeToggle.tsx
│   │   │   └── Video.tsx
│   │   ├── constants/
│   │   │   ├── colors.ts
│   │   │   └── index.ts
│   │   ├── indexer/
│   │   │   ├── abis/
│   │   │   │   └── OurTube.json
│   │   │   ├── build/
│   │   │   │   └── OurTube
│   │   │   ├── generated/
│   │   │   │   └── OurTube
│   │   │   │       ├── schema.ts
│   │   │   ├── schema.graphql
│   │   │   └── subgraph.yaml
│   │   ├── pages/
│   │   │   ├── home/
│   │   │   │   └── index.tsx
│   │   │   ├── upload/
│   │   │   │   └── index.tsx
│   │   │   ├── video/
│   │   │   │   └── [id].tsx
│   │   │   ├── _app.tsx
│   │   │   └── index.tsx
│   │   ├── public/
│   │   │   └── queries/
│   │   │       └── index.ts
│   │   ├── styles/
│   │   │   ├── Home.module.css
│   │   │   └── globals.css
│   │   ├── types/
│   │   │   └── index.ts
│   │   ├── utils/
│   │   │   ├── ThemeContext.tsx
│   │   │   ├── contract.ts
│   │   │   ├── index.ts
│   │   │   └── saveToIPFS.ts
├── lib/
│   ├── getIPFSLink.ts
│   ├── getImage.ts
│   └── getImageKit.ts
├── packages/
├── script/
├── .gitignore
├── Caddyfile
├── Cargo.lock
├── Cargo.toml
├── README.md
├── deploy.sh
├── dfx.json
└── foundry.toml
Installation
To get started with IC-Tube, follow these steps:

Clone the repository:

git clone https://github.com/arhansuba/ic-tube.git
cd ic-tube
Install dependencies for the frontend:

cd frontend
yarn install
Usage
Deploying the Contracts
To deploy the smart contracts, use the provided deploy.sh script or relevant deployment scripts.


bash deploy.sh
Running the Frontend
To start the frontend application:


cd frontend
yarn start
Configuration
Configuration files can be found in the src, frontend, and lib directories. Adjust these files according to your deployment environment and project needs.

Contracts
The smart contracts for IC-Tube are located in the contracts directory:

IcTube.sol: Core contract for managing video uploads and streaming.
Subgraph
The project includes a GraphQL subgraph for querying video data:

schema.graphql: Defines the data schema for the subgraph.
subgraph.yaml: Configuration file for deploying the subgraph.
generated/OurTube/schema.ts: TypeScript types generated from the schema.
Scripts
Scripts for deployment and interactions can be found in the script directory.

Contributing
We welcome contributions to IC-Tube! Please open an issue or submit a pull request on GitHub.

License
This project is licensed under the MIT License. See the LICENSE file for details.

