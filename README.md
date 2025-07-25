﻿# NFT Marketplace Template

A modern, responsive NFT marketplace built with Next.js, Thirdweb, and Chakra UI. This template provides a complete foundation for creating your own NFT marketplace with features like collection browsing, token viewing, user profiles, and marketplace functionality.

## 🚀 Features

### Core Functionality
- **Multi-chain Support**: Built-in support for Ethereum Sepolia, Polygon Amoy, and Avalanche Fuji testnets
- **Collection Browsing**: Explore NFT collections with search, filtering, and sorting capabilities
- **Token Details**: View individual NFT details with attributes and marketplace listings
- **User Profiles**: Browse user profiles and their owned NFTs
- **Marketplace Integration**: Buy, sell, and manage NFT listings
- **ENS Integration**: Support for Ethereum Name Service addresses

### UI/UX Features
- **Responsive Design**: Mobile-first design that works on all devices
- **Dark/Light Mode**: Toggle between dark and light themes
- **Modern UI**: Built with Chakra UI for a polished, professional look
- **Smooth Animations**: Framer Motion powered transitions and interactions
- **Search & Filter**: Advanced search and filtering capabilities
- **Loading States**: Optimized loading experiences throughout the app

### Technical Features
- **TypeScript**: Full TypeScript support for better development experience
- **Performance Optimized**: React Query for efficient data fetching and caching
- **SEO Ready**: Next.js App Router with optimized meta tags
- **Deployment Ready**: Configured for Netlify deployment

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (version 18 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- A code editor (VS Code recommended)

## 🛠️ Installation & Setup

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd nft-marketplace-main
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. Environment Setup

Create a `.env.local` file in the root directory:

```env
# Thirdweb Configuration
NEXT_PUBLIC_THIRDWEB_CLIENT_ID=your_thirdweb_client_id
NEXT_PUBLIC_THIRDWEB_SECRET_KEY=your_thirdweb_secret_key

# Optional: Custom RPC URLs
NEXT_PUBLIC_ETHEREUM_RPC_URL=your_ethereum_rpc_url
NEXT_PUBLIC_POLYGON_RPC_URL=your_polygon_rpc_url
NEXT_PUBLIC_AVALANCHE_RPC_URL=your_avalanche_rpc_url
```

### 4. Configure Your Collections

Edit `src/consts/nft_contracts.ts` to add your NFT collections:

```typescript
export const NFT_CONTRACTS: NftContract[] = [
  {
    address: "your_contract_address",
    chain: sepolia, // or other supported chains
    title: "Your Collection Name",
    description: "Collection description",
    thumbnailUrl: "your_thumbnail_url",
    type: "ERC721", // or "ERC1155"
  },
  // Add more collections...
];
```

### 5. Run the Development Server

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## 🏗️ Project Structure

```
marketplace-template-main/
├── src/
│   ├── app/                    # Next.js App Router pages
│   │   ├── collection/         # Collection pages
│   │   ├── collections/        # Collections listing page
│   │   ├── profile/           # User profile pages
│   │   └── page.tsx           # Homepage
│   ├── components/            # React components
│   │   ├── collection-page/   # Collection-specific components
│   │   ├── profile-page/      # Profile-specific components
│   │   ├── shared/           # Shared components (Navbar, etc.)
│   │   └── token-page/       # Token-specific components
│   ├── consts/               # Constants and configuration
│   ├── extensions/           # Thirdweb extensions
│   └── hooks/               # Custom React hooks
├── public/                  # Static assets
└── package.json            # Dependencies and scripts
```

## 🎨 Customization

### Styling
The project uses Chakra UI with a custom theme. You can customize the theme in `src/consts/chakra.ts`.

### Adding New Chains
To add support for new blockchain networks, edit `src/consts/chains.ts`:

```typescript
import { defineChain } from "thirdweb";

export const yourCustomChain = defineChain({
  id: 1,
  name: "Your Chain",
  nativeCurrency: { name: "ETH", symbol: "ETH", decimals: 18 },
  rpc: "your_rpc_url",
});
```

### Adding New Features
The modular structure makes it easy to add new features:
- Add new pages in `src/app/`
- Create reusable components in `src/components/`
- Add custom hooks in `src/hooks/`

## 🚀 Deployment

### Netlify Deployment

1. Connect your repository to Netlify
2. Set build command: `npm run build`
3. Set publish directory: `.next`
4. Add environment variables in Netlify dashboard
5. Deploy!

### Vercel Deployment

1. Install Vercel CLI: `npm i -g vercel`
2. Run: `vercel`
3. Follow the prompts to deploy

## 📱 Screenshots

### Homepage
![Homepage](https://github.com/user-attachments/assets/bf672748-9a30-4a5e-b4db-03f2c72028b4)
*Landing page with trending collections and featured NFTs*

### Collection Detail
![Collection Detail](https://github.com/user-attachments/assets/06b4417f-63c8-4c42-8c24-d4bce60ed13a)
*Individual collection page with NFT grid*

### Token Page
![Token Page](https://github.com/user-attachments/assets/425d5cb4-57b3-4b86-bf3d-8a69e7085f0b)
*Detailed view of individual NFT with marketplace options*

### User Profile
![User Profile](https://github.com/user-attachments/assets/9555dd92-3c70-4e80-ae60-29d9230d58b6)
*User profile showing owned NFTs and collections*


## 🔧 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


## Acknowledgments

- [Thirdweb](https://thirdweb.com/) for the Web3 infrastructure
- [Chakra UI](https://chakra-ui.com/) for the component library
- [Next.js](https://nextjs.org/) for the React framework
- [Framer Motion](https://www.framer.com/motion/) for animations

---

**Happy Building! 🚀**
