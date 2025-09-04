# Divine Sun C376 - Cloudflare Workers Project

A TypeScript-based Cloudflare Workers application with KV storage and environment-specific configurations.

## 🚀 Quick Deploy

Deploy this project to Cloudflare Workers with one click:

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/deloreyj/d2c-with-environments)

## ✨ Features

- **TypeScript Support**: Full TypeScript development experience
- **KV Storage**: Configured with Cloudflare KV namespace binding
- **Environment Management**: Separate production environment with custom domain
- **Testing**: Vitest setup with Cloudflare Workers testing pool
- **Development Tools**: Hot reload with Wrangler dev server

## 🏗️ Project Structure

```
├── src/
│   └── index.ts          # Main Worker entry point
├── test/
│   ├── index.spec.ts     # Test files
│   └── tsconfig.json     # Test TypeScript config
├── package.json          # Dependencies and scripts
├── wrangler.jsonc        # Cloudflare Workers configuration
├── tsconfig.json         # TypeScript configuration
└── vitest.config.mts     # Vitest configuration
```

## 🛠️ Development

### Prerequisites

- Node.js (v18 or later)
- npm or yarn
- Cloudflare account

### Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/deloreyj/d2c-with-environments.git
   cd d2c-with-environments
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open your browser to `http://localhost:8787` to see your Worker in action.

### Available Scripts

- `npm run dev` - Start development server
- `npm run deploy` - Deploy to Cloudflare Workers
- `npm run test` - Run tests with Vitest
- `npm run cf-typegen` - Generate TypeScript types for Wrangler

## 🌍 Environments

### Development
- Local development server on `localhost:8787`
- Uses local KV namespace for testing

### Production
- Custom domain: `production-d2c-test.honeygrid.io`
- Production KV namespace
- Observability enabled

## 📦 Resources

This project uses the following Cloudflare resources:

- **KV Namespace**: `my_cool_namespace` - Key-value storage for your application data
- **Custom Domain**: Production environment accessible via custom domain
- **Observability**: Monitoring and analytics enabled

## 🚀 Deployment

### Manual Deployment

```bash
npm run deploy
```

### Automatic Deployment

Use the "Deploy to Cloudflare" button above for one-click deployment. This will:

1. Clone this repository to your GitHub account
2. Automatically provision required Cloudflare resources (KV namespace)
3. Deploy the Worker to the Cloudflare network
4. Set up the production environment with custom domain

## 🧪 Testing

Run the test suite:

```bash
npm test
```

Tests are configured to run against the Cloudflare Workers runtime using `@cloudflare/vitest-pool-workers`.

## 📝 Configuration

The Worker configuration is managed in `wrangler.jsonc`. Key settings include:

- **Account ID**: Your Cloudflare account identifier
- **Compatibility Date**: Ensures consistent Worker behavior
- **KV Bindings**: Storage namespace configuration
- **Environment Variables**: Separate configs for different environments

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Run the test suite
6. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 🔗 Links

- [Cloudflare Workers Documentation](https://developers.cloudflare.com/workers/)
- [Wrangler CLI Documentation](https://developers.cloudflare.com/workers/wrangler/)
- [KV Storage Documentation](https://developers.cloudflare.com/kv/)
