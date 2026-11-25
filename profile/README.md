<p align="center">
  <a href="https://www.merkaly.io">
    <img src="assets/banner.jpg" alt="Merkaly: dropshipping stores for Brazil, from product to payment" width="100%">
  </a>
</p>

<p align="center">
  <strong>Merkaly is a dropshipping platform for online stores in Brazil.</strong><br>
  <em>Sua loja de dropshipping, do produto ao pagamento.</em>
</p>

<p align="center">
  <a href="https://www.merkaly.io">Website</a> ·
  <a href="https://docs.merkaly.io">Docs</a> ·
  <a href="https://www.linkedin.com/company/merkaly.io">LinkedIn</a> ·
  <a href="mailto:support@merkaly.io">support@merkaly.io</a>
</p>

## What Merkaly does

- **Import products** from international suppliers with their photos, variants and cost, then set your margin.
- **Sell in your own store** on your own domain, built for the Brazilian market (pt-BR, BRL).
- **Get paid with Pix and card**, with no commission on the sale value.
- **Order from the supplier in one click** using the buyer's data; tracking reaches the buyer automatically.
- **Run everything from one control tower**: each order shows its status from payment to delivery, real cost, profit and the next action.

No inventory and no spreadsheets. Plans: **Free** (with ads, no own domain), **per product sold** (R$ 10 per distinct product sold in the month, taken from the profit, own domain) and **fixed** (R$ 500 per month, all included, priority support).

<p align="center">
  <img src="assets/admin-orders.png" alt="Merkaly admin: orders list with status, customer and total" width="100%">
</p>

## How it works

1. **Import.** Pick products from a supplier and bring them into your catalog with photos, variants and cost.
2. **Sell.** Your storefront is live on your domain and the buyer pays with Pix or card.
3. **Order in one click.** Merkaly places the supplier order with the buyer's data and keeps you and the buyer posted until delivery.

## Surfaces

| Surface | What it is |
| --- | --- |
| [www.merkaly.io](https://www.merkaly.io) | Marketing site and self-service signup |
| [admin.merkaly.io](https://admin.merkaly.io) | Merchant admin, the control tower |
| Storefronts | Each merchant's own store, on `*.merkaly.store` or their own domain |
| dashboard.merkaly.io | Merkaly's internal operations panel |
| [docs.merkaly.io](https://docs.merkaly.io) | How Merkaly works: glossary, animated flows, lifecycles and decisions by domain |

## Services

| Service | Role |
| --- | --- |
| api.merkaly.io | Records and business rules: catalog, orders, finance, accounts |
| payments.merkaly.io | The only service that talks to the payment provider; stateless |
| webhooks.merkaly.io | Entry gate for external providers (payments, identity, supplier); delivers each message to its domain's exchange |
| signals.merkaly.io | Notifications (email) |
| auth.merkaly.io | Auth0 tenant as code |

Services talk over RabbitMQ: one exchange per domain (`merkaly.<service>`), events, commands and request-reply invokes. See the [messaging flows](https://docs.merkaly.io/flujos).

## Stack

- **Frontends:** Nuxt 4, Vue 3, Bootstrap 5 ([bootstrap-vue-next](https://bootstrap-vue-next.github.io/bootstrap-vue-next/)); docs on Docus
- **Backend:** NestJS and MongoDB, with a database per tenant
- **Identity:** Auth0 (organizations per store)
- **Messaging:** RabbitMQ
- **Hosting:** Railway
- **Packages:** [`@merkaly/api`](https://github.com/merkaly-io/api) (shared contracts), [`@merkaly/nuxt`](https://github.com/merkaly-io/nuxt), [`@merkaly/nest`](https://github.com/merkaly-io/nest)

## Contact

- Support: [support@merkaly.io](mailto:support@merkaly.io)
- Sales: [sales@merkaly.io](mailto:sales@merkaly.io)
