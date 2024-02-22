<a href="https://app.vercel.pub">
  <img alt="Platforms Starter Kit" src="/public/thumbnail.png">
  <h1 align="center">Eco Ops Platforms Starter Kit</h1>
</a>

<p align="center">
  The <em>all-in-one</em> starter kit <br/>
  for biodivertity token valuation and energy efficient FOSS cNfT infrastructure.
</p>

<p align="center">
  <a href="#introduction"><strong>Introduction</strong></a> ·
  <a href="https://app.vercel.pub/"><strong>Demo</strong></a> ·
  <a href="#deploy-your-own"><strong>Deploy Your OwnBiodiverity Token </strong></a> ·
  <a href="https://vercel.com/guides/nextjs-multi-tenant-application"><strong>Guide</strong></a> ·
    <a href="https://vercel.com/guides/nextjs-multi-tenant-application"><strong>Bubble Gum Tree</strong></a> ·

  <a href="https://steven.vercel.pub/kitchen-sink"><strong>Kitchen Sink</strong></a> ·
  <a href="#contributing"><strong>Contributing</strong></a>
</p>
<br/>

## Introduction

The [Platforms Starter Kit](https://app.vercel.pub/) is a full-stack Next.js app with multi-tenancy and custom domain support. Built with [Next.js App Router](https://nextjs.org/docs/app), [Vercel Postgres](https://vercel.com/storage/postgres) and the [Vercel Domains API](https://vercel.com/docs/rest-api/endpoints#domains).

Here's a quick 30-second demo:

https://github.com/vercel/platforms/assets/28986134/bd370257-0c27-4cf5-8a56-28589f36f0ef

## Features

1. **Multi-tenancy:** Programmatically assign unlimited custom domains, subdomains, and SSL certificates to your users using the [Vercel Domains API](https://vercel.com/docs/rest-api/endpoints#domains)
2. **Performance**: Fast & beautiful blog posts cached via [Vercel's Edge Network](https://vercel.com/docs/concepts/edge-network/overview), with the ability to invalidate the cache on-demand (when users make changes) using [Incremental Static Regeneration](https://vercel.com/docs/concepts/next.js/incremental-static-regeneration) + Next.js' `revalidateTag` API
3. **AI Editor**: AI-powered Markdown editor for a Notion-style writing experience powered by [Novel](https://novel.sh/)
4. **Image Uploads**: Drag & drop / copy & paste image uploads, backed by [Vercel Blob](https://vercel.com/storage/blob)
5. **Custom styles**: Custom fonts, 404 pages, favicons, sitemaps for each site via the [Next.js file-based Metadata API](https://nextjs.org/docs/app/api-reference/file-conventions/metadata)
6. **Dynamic OG Cards**: Each blog post comes with a dynamic OG image powered by [@vercel/og](https://vercel.com/docs/concepts/functions/edge-functions/og-image-generation)
7. **Dark Mode**: For a better user experience at night
8. **Multi-tenant Preview URLs**: Preview changes to your client sites using [Vercel Preview URLs](https://vercel.com/docs/deployments/generated-urls). [Learn more](https://vercel.com/guides/nextjs-multi-tenant-application#3.-multi-tenant-preview-urls).

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://images.ctfassets.net/e5382hct74si/k7XpXIE0rDsHCAYvkKhff/ff44c07588068d8fefa334cd6a318c8a/CleanShot_2023-07-05_at_08.39.02.png">
    <source media="(prefers-color-scheme: light)" srcset="https://images.ctfassets.net/e5382hct74si/7tiAitb8kdgUGktycr540c/d33f2834f9356bce25e0721c4ebe4f9a/CleanShot_2023-07-05_at_08.39.10.png">
    <img alt="Demo" src="https://images.ctfassets.net/e5382hct74si/7tiAitb8kdgUGktycr540c/d33f2834f9356bce25e0721c4ebe4f9a/CleanShot_2023-07-05_at_08.39.10.png">
</picture>

## Deploy Your Own

Deploy your own version of this starter kit with Vercel.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?demo-title=Platforms+Starter+Kit&demo-description=A+template+for+site+builders+and+low-code+tools.&demo-url=https%3A%2F%2Fdemo.vercel.pub%2F&demo-image=%2F%2Fimages.ctfassets.net%2Fe5382hct74si%2F40JwjdHlPr0Z575MPYbxUA%2Fd5903afc68cb34569a3886293414c37c%2FOG_Image.png&project-name=Platforms+Starter+Kit&repository-name=platforms-starter-kit&repository-url=https%3A%2F%2Fgithub.com%2Fvercel%2Fplatforms&from=templates&env=NEXT_PUBLIC_ROOT_DOMAIN%2CNEXTAUTH_SECRET%2CAUTH_GITHUB_ID%2CAUTH_GITHUB_SECRET%2CAUTH_BEARER_TOKEN%2CPROJECT_ID_VERCEL%2CTEAM_ID_VERCEL%2COPENAI_API_KEY&envDescription=These+environment+variables+are+required+to+run+this+application.&envLink=https%3A%2F%2Fgithub.com%2Fvercel%2Fplatforms%2Fblob%2Fmain%2F.env.example&stores=%5B%7B%22type%22%3A%22postgres%22%7D%5D)

You can also [read the guide](https://vercel.com/guides/nextjs-multi-tenant-application) to learn how to develop your own version of this template.

## What is a multi-tenant application?

Multi-tenant applications serve multiple customers across different subdomains/custom domains with a single unified codebase.

For example, our demo is a multi-tenant application:

- Subdomain: [demo.vercel.pub](http://demo.vercel.pub)
- Custom domain: [platformize.co](http://platformize.co) (maps to [demo.vercel.pub](http://demo.vercel.pub))
- Build your own: [app.vercel.pub](http://app.vercel.pub)

Another example is [Hashnode](https://vercel.com/customers/hashnode), a popular blogging platform. Each writer has their own unique `.hashnode.dev` subdomain for their blog:

- [eda.hashnode.dev](https://eda.hashnode.dev/)
- [katycodesstuff.hashnode.dev](https://katycodesstuff.hashnode.dev/)
- [akoskm.hashnode.dev](https://akoskm.hashnode.dev/)

Users can also map custom domains to their `.hashnode.dev` subdomain:

- [akoskm.com](https://akoskm.com/) → [akoskm.hashnode.dev](https://akoskm.hashnode.dev/)

With the Platforms Starter Kit, you can offer unlimited custom domains at no extra cost to your customers as a premium feature, without having to worry about custom nameservers or configuring SSL certificates.

## Examples of platforms

Vercel customers like [Hashnode](https://vercel.com/customers/hashnode), [Super](https://super.so), and [Cal.com](https://cal.com) are building scalable platforms on top of Vercel and Next.js. There are multiple types of platforms you can build with this starter kit:

### 1. Content creation platforms

These are content-heavy platforms (blogs) with simple, standardized page layouts and route structure.

> “With Vercel, we spend less time managing our infrastructure and more time delivering value to our users.” — Sandeep Panda, Co-founder, Hashnode

1. [Hashnode](https://hashnode.com)
2. [Mintlify](https://mintlify.com/)
3. [Read.cv](https://read.cv/)

### 2. Website & e-commerce store builders

No-code site builders with customizable pages.

By using Next.js and Vercel, [Super](https://super.so/) has fast, globally distributed websites with a no-code editor (Notion). Their customers get all the benefits of Next.js (like [Image Optimization](https://nextjs.org/docs/basic-features/image-optimization)) without touching any code.

1. [Super.so](https://super.so)
2. [Typedream](https://typedream.com)
3. [Makeswift](https://www.makeswift.com/)

### 3. B2B2C platforms

Multi-tenant authentication, login, and access controls.

With Vercel and Next.js, platforms like [Instatus](https://instatus.com) are able to create status pages that are _10x faster_ than competitors.

1. [Instatus](https://instatus.com/)
2. [Cal.com](https://cal.com/)
3. [Dub](https://dub.co/)

## Built on open source

This working demo site was built using the Platforms Starter Kit and:

- [Next.js](https://nextjs.org/) as the React framework
- [Tailwind](https://tailwindcss.com/) for CSS styling
- [Prisma](https://prisma.io/) as the ORM for database access
- [Novel](https://novel.sh/) for the WYSIWYG editor
- [Vercel Postgres](https://vercel.com/storage/postgres) for the database
- [Vercel Blob](https://vercel.com/storage/blob) for image uploads
- [NextAuth.js](https://next-auth.js.org/) for authentication
- [Tremor](https://tremor.so/) for charts
- [Vercel](http://vercel.com/) for deployment

## Contributing

- [Start a discussion](https://github.com/vercel/platforms/discussions) with a question, piece of feedback, or idea you want to share with the team.
- [Open an issue](https://github.com/vercel/platforms/issues) if you believe you've encountered a bug with the starter kit.

## Author

- G Willon ([](https://twitter.com/ecociy))

- Steven Tey ([@steventey](https://twitter.com/steventey))


## project advice from GPT4

1. Objectives and Scope

    Clearly define the problem you're trying to solve and the impact you wish to have in each of the countries you've mentioned. This will help in keeping the project focused and measurable.

2. Use Agile Development Methodologies

    Adopt an agile development approach, which allows for iterative and incremental development. This approach will enable you to rapidly prototype, test, and refine your solution based on feedback.

3. Leverage Existing Tools and Platforms

    Utilize existing blockchain networks, like Solana, which is known for its high throughput and low transaction costs, making it suitable for handling large-scale and high-frequency data.
    For decentralized storage, IPFS and nft.storage are great choices. nft.storage specifically provides free storage for NFT metadata and assets and is backed by IPFS and Filecoin.

4. Build a Modular Architecture

    Design your system in a modular way, where each component (like data ingestion, Merkle tree construction, IPFS storage, and Solana blockchain interaction) is a separate module. This allows for easier testing, updating, and scaling of each module.

5. Focus on Data Minimization and Privacy

    Since you're dealing with potentially sensitive ecological data, ensure your design adheres to data minimization principles. Store only what's necessary on-chain, and use pointers to off-chain storage like IPFS for detailed data.

6. Engage with the Community

    Since your project has a global impact, engage with local communities and stakeholders in each of the countries you've mentioned. They can provide valuable insights and help tailor your solution to local needs.

7. Secure and Optimize Smart Contracts

    Given the critical nature of your application, ensure that your smart contracts on Solana are well-audited, secure, and optimized for performance and cost.

8. Test Thoroughly

    Test your prototype extensively in different environments to ensure its robustness, scalability, and usability. Consider both technical tests (like load testing and smart contract audits) and user acceptance testing to gather feedback on usability.

9. Documentation and Training

    Create comprehensive documentation for your system and provide training resources to help onboard new users and developers, especially in the diverse regions you aim to impact.

10. Seek Partnerships and Funding

    Look for partnerships with environmental organizations, governments, and tech companies in the regions of interest. They can provide funding, resources, and a network to scale your solution.

11. Implement Monitoring and Analytics

    Implement monitoring and analytics tools to track the usage, performance, and impact of your solution. This data will be invaluable for reporting to stakeholders and for continuous improvement.

12. Stay Adaptable and Open to Feedback

    Be prepared to pivot or adapt your solution based on feedback and new findings as you progress. The field of blockchain and decentralized storage is rapidly evolving, so staying flexible is key.

## License

The MIT License.

---

<a aria-label="Vercel logo" href="https://vercel.com">
  <img src="https://badgen.net/badge/icon/Made%20by%20Vercel?icon=zeit&label&color=black&labelColor=black">
</a>
