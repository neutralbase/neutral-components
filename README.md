<div align="center">

<img src="./neutral-components.png" alt="Neutral Components" width="600" />

### ⭐ Star this repo to stay up to date with future releases ⭐

</div>

# Neutral Components

The shadcn for backend. Build production-ready AI applications with Convex components.

## What is this?

Neutral Components is a collection of Convex components that handle the hard parts of building AI-powered applications. Each component is independent, well-tested, and designed to work seamlessly together.

Think shadcn/ui, but for your backend infrastructure.

## Components

| Component                                                     | npm                                                                                             | Description                                                       | Status      |
| ------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- | ----------- |
| [neutral-cost](https://github.com/neutralbase/neutral-cost)   | [![npm](https://img.shields.io/npm/v/neutral-cost)](https://www.npmjs.com/package/neutral-cost) | Track AI and tool costs, manage credits, bill customers           | ✅ Released |
| [neutral-tools](https://github.com/neutralbase/neutral-tools) | [neutral-tools](https://www.npmjs.com/package/neutral-tools)                                    | Write tools once, run in any AI framework (AI SDK, Pipecat, etc.) | Coming Soon |
| [neutral-files](https://github.com/neutralbase/neutral-files) | [neutral-files](https://www.npmjs.com/package/neutral-files)                                    | Unified S3-compatible API for all storage providers               | Coming Soon |
| [neutral-agent](https://github.com/neutralbase/neutral-agent) | [neutral-agent](https://www.npmjs.com/package/neutral-agent)                                    | Production patterns for internal and user-facing agents           | Coming Soon |
| [neutral-vfs](https://github.com/neutralbase/neutral-vfs)     | [neutral-vfs](https://www.npmjs.com/package/neutral-vfs)                                        | Virtual file system for coding agents and sandboxes               | Coming Soon |

## CLI

| Tool                                                      | npm                                                      | Description                                       | Status      |
| --------------------------------------------------------- | -------------------------------------------------------- | ------------------------------------------------- | ----------- |
| [neutral-cli](https://github.com/neutralbase/neutral-cli) | [neutral-cli](https://www.npmjs.com/package/neutral-cli) | Superset of shadcn CLI with Convex code insertion | Coming Soon |

## Why Convex Components?

Convex components provide true isolation - each component runs in its own namespace with its own tables and functions. This means:

- **No conflicts** - Components can't accidentally interfere with your app or each other
- **Easy upgrades** - Update components independently without migrations
- **Type safety** - Full TypeScript support with generated types
- **Real-time by default** - All queries are live and reactive

## Getting Started

1. Set up a Convex project if you haven't already:

   ```sh
   npm create convex
   ```

2. Install any component:

   ```sh
   npm install neutral-cost
   ```

3. Add it to your `convex/convex.config.ts`:

   ```ts
   import { defineApp } from "convex/server";
   import costComponent from "neutral-cost/convex.config";

   const app = defineApp();
   app.use(costComponent);

   export default app;
   ```

4. Start using it in your functions.

## Philosophy

- **Composable** - Use one component or all of them
- **Escape hatches** - Extend functionality with neutral-cli when needed
- **Production-ready** - Built for real workloads, not demos
- **Open source** - FSL-1.1-ALv2 licensed (Apache 2.0 after 2 years)

## Links

- [Convex](https://convex.dev) - The backend platform these components run on
- [Convex Components Docs](https://docs.convex.dev/components) - Learn more about the component system

## License

All components are licensed under [FSL-1.1-ALv2](https://fsl.software/FSL-1.1-ALv2.template.md) - Functional Source License with Apache 2.0 future license.
