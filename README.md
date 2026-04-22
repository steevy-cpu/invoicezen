# InvoiceZen

**Free invoice generator. No account. No tracking. Direct PDF download.**

→ **Live:** https://steevy-cpu.github.io/invoicezen/

---

## The Problem

Every free invoice tool online requires you to create an account before you can generate a single PDF. The best free alternative — invoice-generator.com — requires you to enter your email address just to receive your invoice. Wave, Zoho, FreshBooks, HoneyBook, Bonsai: all require accounts.

This is friction that serves the tool, not the user. A freelancer who needs to invoice a client right now should be able to do it in under 60 seconds, close the tab, and move on.

## Who It's For

- Freelancers sending their first invoice and not wanting to commit to a platform
- Independent contractors who bill occasionally and don't want a subscription
- Anyone who needs a quick, clean PDF invoice without creating yet another account

## Why Existing Tools Fail

| Tool | Problem |
|------|---------|
| Wave | Account required |
| Zoho Invoice | Account required |
| FreshBooks | Paid + account |
| Invoice Ninja | Self-hosted or account |
| invoice-generator.com | Requires your email to send the PDF |
| PayPal/Stripe invoicing | Account + platform lock-in |

## How InvoiceZen Wins

- **No account** — open the URL, fill the form, download the PDF
- **No email required** — your invoice downloads directly to your device
- **Zero tracking** — no analytics, no cookies, no external requests
- **Remembers you** — opt-in localStorage saves your business info locally, never uploaded
- **Works offline** — after first load, no internet needed
- **Auto-increments** — invoice numbers go up automatically
- **Mobile-first** — fully usable on phone with tab-based UI

**Success metric: Invoice created and downloaded in under 60 seconds.**

## Technical Details

- Single `index.html` file — no build step, no dependencies, no CDN
- All PDF generation via browser's native print-to-PDF (zero library, zero external calls)
- ~28KB total page weight
- MIT licensed

## Getting First 100 Users

**The post:**
> *r/freelance — "I built a free invoice generator with no account required (just fill and download)"*

r/freelance has 350k+ members and threads about invoice tools get 200+ upvotes regularly. The post angle: show the before/after of having to sign up for Wave vs. landing on InvoiceZen. Post Monday morning when freelancers are thinking about billing.

**Secondary channels:**
1. **r/Entrepreneur** — "I got tired of every free invoice tool requiring sign-up, so I made one that doesn't"
2. **HN Show HN** — "Show HN: Invoice generator with no account, no email, direct PDF (single HTML file)"
3. **r/webdev** — "Made a single-file invoice generator — no build step, no dependencies, no tracking"
4. **Indie Hackers** — post in the "Products" section; freelance tool targeting is strong there

## What's Next at 10k Users

1. **Multiple templates** — a minimal template, a creative agency template, a consulting template
2. **Logo upload** — drag-and-drop logo (stored in localStorage as base64)
3. **Saved clients** — localStorage client list for repeat billing
4. **Recurring invoices** — duplicate last invoice with auto-incremented number
5. **Multi-page support** — automatic page breaks for invoices with many line items
6. **Export as PNG** — for platforms that don't accept PDF attachments

## Tradeoffs Made

- **Browser print dialog vs. one-click download**: Browser print-to-PDF produces perfectly searchable, styled output with zero library weight. The tradeoff is one extra user action (clicking "Save as PDF" in the print dialog). Considered jsPDF/html2canvas but the output quality is lower and it adds ~400KB.
- **No templates yet**: Focus on one thing done well over feature breadth. The clean blue-header template covers 90% of use cases.
- **No send-by-email**: Keeps the tool server-free and privacy-pure. Users can attach the PDF to their own email.

## License

MIT
