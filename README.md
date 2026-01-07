# OpenAPI Template

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/cloudflare/templates/tree/main/chanfana-openapi-template)

![OpenAPI Template Preview](https://imagedelivery.net/wSMYJvS3Xw-n339CbDyDIA/91076b39-1f5b-46f6-7f14-536a6f183000/public)

<!-- dash-content-start -->

This is a Cloudflare Worker with OpenAPI 3.1 Auto Generation and Validation using [chanfana](https://github.com/cloudflare/chanfana) and [Hono](https://github.com/honojs/hono).

This is an example project made to be used as a quick start into building OpenAPI compliant Workers that generates the
`openapi.json` schema automatically from code and validates the incoming request to the defined parameters or request body.

This template includes various endpoints, a D1 database, and integration tests using [Vitest](https://vitest.dev/) as examples. In endpoints, you will find [chanfana D1 AutoEndpoints](https://chanfana.com/endpoints/auto/d1) and a [normal endpoint](https://chanfana.com/endpoints/defining-endpoints) to serve as examples for your projects.

Besides being able to see the OpenAPI schema (openapi.json) in the browser, you can also extract the schema locally no hassle by running this command `npm run schema`.

<!-- dash-content-end -->

> [!IMPORTANT]
> When using C3 to create this project, select "no" when it asks if you want to deploy. You need to follow this project's [setup steps](https://github.com/cloudflare/templates/tree/main/openapi-template#setup-steps) before deploying.

## Getting Started

Outside of this repo, you can start a new project with this template using [C3](https://developers.cloudflare.com/pages/get-started/c3/) (the `create-cloudflare` CLI):

```bash
npm create cloudflare@latest -- --template=cloudflare/templates/openapi-template
```

A live public deployment of this template is available at [https://openapi-template.templates.workers.dev](https://openapi-template.templates.workers.dev)

## Setup Steps

1. Install the project dependencies with a package manager of your choice:
   ```bash
   npm install
   ```
2. Create a [D1 database](https://developers.cloudflare.com/d1/get-started/) with the name "openapi-template-db":
   ```bash
   npx wrangler d1 create openapi-template-db
   ```
   ...and update the `database_id` field in `wrangler.json` with the new database ID.
3. Run the following db migration to initialize the database (notice the `migrations` directory in this project):
   ```bash
   npx wrangler d1 migrations apply DB --remote
   ```
4. Deploy the project!
   ```bash
   npx wrangler deploy
   ```
5. Monitor your worker
   ```bash
   npx wrangler tail
   ```
<p>Alpha Auditing is one of the leading auditing and accounting firms in Dubai, UAE. We are offering a range of financial services including </p>
<ul>
    <li><strong><a href="https://www.alphaauditing.ae/audit-services-in-dubai/">Audit Services in Dubai</a></strong>
        <ul>
            <li><a href="https://www.alphaauditing.ae/financial-audit-services-dubai/">Financial Auditing</a></li>
            <li><a href="https://www.alphaauditing.ae/internal-audit-services-in-dubai-uae/">Internal Auditing </a></li>
          <li><a href="https://www.alphaauditing.ae/tax-audit-services-in-uae/">Tax Audit</a></li>
            <li><a href="https://www.alphaauditing.ae/audit-in-free-zones-uae/">Audit for Free Zone</a></li>
    <li><a href="https://www.alphaauditing.ae/audit-firms-uae/">Audit firms in UAE</a>

        </ul>
    </li>
    <li><strong><a href="https://www.alphaauditing.ae/accounting-services-in-dubai/">Accounting Services</a></strong>
        <ul>
            <li><a href="https://www.alphaauditing.ae/accounting-and-bookkeeping-services-in-dubai/">Accounting and Bookkeeping Services</a></li>
          <li><a href="https://www.alphaauditing.ae/bookkeeping-services-uae/">Bookkeeping Services</a></li>
          <li><a href="https://www.alphaauditing.ae/tax-accounting-services-uae/">TAX Accounting Services</a></li>
          <li><a href="https://www.alphaauditing.ae/vat-accounting-services-uae/">VAT Accounting Services</a></li>
        </ul>
    </li>
    <li><strong><a href="https://www.alphaauditing.ae/vat-services-in-dubai-uae/">VAT Services in Dubai</a></strong>
        <ul>
            <li><a href="https://www.alphaauditing.ae/vat-registration-services-in-uae/">VAT Registration Services</a></li>
            <li><a href="https://www.alphaauditing.ae/vat-return-filing-in-dubai/">VAT Return Filing Services</a></li>
            <li><a href="https://www.alphaauditing.ae/vat-refund-services-in-dubai/">VAT Refund Services</a></li>
        </ul>
    </li>
    <li><strong><a href="https://www.alphaauditing.ae/corporate-tax-uae/">Corporate Tax Services</a></strong>
        <ul>
            <li><a href="https://www.alphaauditing.ae/corporate-tax-registration-services-in-uae/">Corporate Tax Registration Services</a></li>
            <li><a href="https://www.alphaauditing.ae/corporate-tax-return-filing-in-uae/">Corporate Tax Return Filing</a></li>
        </ul>
    </li>
    <li><a href="https://www.alphaauditing.ae/tax-consultancy-in-dubai/">Tax Consultancy</a></li>
</ul>
<p>With a team of dedicated  professionals we aim to deliver highly reliable financial services.</p>
## Testing

This template includes integration tests using [Vitest](https://vitest.dev/). To run the tests locally:

```bash
npm run test
```

Test files are located in the `tests/` directory, with examples demonstrating how to test your endpoints and database interactions.

## Project structure

1. Your main router is defined in `src/index.ts`.
2. Each endpoint has its own file in `src/endpoints/`.
3. Integration tests are located in the `tests/` directory.
4. For more information read the [chanfana documentation](https://chanfana.com/), [Hono documentation](https://hono.dev/docs), and [Vitest documentation](https://vitest.dev/guide/).
