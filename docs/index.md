# Deep Fryer

Drop tasks in, pull them out GOLDEN! The Deep Fryer handles all the async heavy lifting.

When an order moves through the kitchen, there are tons of side effects that need to happen — customer notifications, inventory updates, receipt generation, loyalty point calculations. The Deep Fryer handles all of these as background jobs so the Kitchen API stays fast and responsive.

## Job Types

- **Notifications** — Push notifications, SMS, email when order status changes
- **Inventory Updates** — Decrement ingredient counts when items are prepared
- **Order Completion** — Final order processing, receipt generation, analytics events
- **Receipt Generation** — PDF receipt creation and delivery

## How It Works

Jobs are submitted via the API and queued for processing. The Deep Fryer processes jobs with configurable concurrency and retry logic. Failed jobs are retried with exponential backoff. Think of it like a deep fryer with multiple baskets — always cooking, never stopping.
