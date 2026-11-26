# SixtyNet VPS: What Residential IP Costs Now, Why Ports 80/443 Are Closed, and Which Plan Fits (All 13 Plans Priced)

SixtyNet's residential IP VPS starts at **$260 per year**. That's Residential-STARTER: 2 cores, 2GB RAM, 40GB NVMe, 5TB of traffic. The plain Los Angeles LAX line starts lower at **$200 per year**. All four residential plans ship with ports 80 and 443 closed, so none of them can host a public website. LAX is the line built for that job.

Everything below comes from the official plan page as it stands today: the full 13-plan price list, the restrictions that decide whether a residential plan is usable for your workload, and the reason a lot of recent reviews still quote prices SixtyNet no longer charges.

> **Most people who need a residential IP:** Residential-MICRO at **$460/year** (4 cores, 4GB RAM, 80GB NVMe, 10TB traffic). It's the tier where social media tools, scrapers and multi-account setups stop competing for RAM.
> **Most people who just need a US VPS:** LAX-STARTER at **$200/year**, DDoS protection included, no port restrictions.
> 👉 [Check the live SixtyNet plan list and current pricing](https://sixtynet.net/aff.php?aff=39)

## All 13 SixtyNet plans, with current annual prices

Every plan below is billed annually and priced in USD. The number in brackets is the official list price before the annual discount is applied. Residential and IRVINE-PRO plans are grouped together at the top because they share the residential IP attribute; LAX and Storage share the DDoS-protected standard network; the China Unicom plan is its own thing entirely.

| Plan | vCPU / RAM / NVMe | Traffic | Annual price | Order |
| --- | --- | --- | --- | --- |
| Residential-STARTER | 2 / 2GB / 40GB | 5TB | $260 (list $300) | [Order Residential-STARTER](https://sixtynet.net/aff.php?aff=39) |
| Residential-MICRO | 4 / 4GB / 80GB | 10TB | $460 (list $540) | [Order Residential-MICRO](https://sixtynet.net/aff.php?aff=39) |
| Residential-MEDIUM | 8 / 8GB / 160GB | 20TB | $860 (list $1,020) | [Order Residential-MEDIUM](https://sixtynet.net/aff.php?aff=39) |
| Residential-LARGE | 16 / 16GB / 320GB | 40TB | $1,660 (list $1,980) | [Order Residential-LARGE](https://sixtynet.net/aff.php?aff=39) |
| IRVINE-PRO-STARTER | 2 / 2GB / 40GB | 5TB | $350 (list $420) | [Order IRVINE-PRO-STARTER](https://sixtynet.net/aff.php?aff=39) |
| IRVINE-PRO-MICRO | 4 / 4GB / 80GB | 10TB | $550 (list $660) | [Order IRVINE-PRO-MICRO](https://sixtynet.net/aff.php?aff=39) |
| LAX-STARTER | 2 / 2GB / 40GB | 5TB | $200 (list $240) | [Order LAX-STARTER](https://sixtynet.net/aff.php?aff=39) |
| LAX-MICRO | 4 / 4GB / 80GB | 10TB | $400 (list $480) | [Order LAX-MICRO](https://sixtynet.net/aff.php?aff=39) |
| LAX-MEDIUM | 8 / 8GB / 160GB | 20TB | $800 (list $960) | [Order LAX-MEDIUM](https://sixtynet.net/aff.php?aff=39) |
| LAX-LARGE | 8 / 16GB / 320GB | 40TB | $1,600 (list $1,920) | [Order LAX-LARGE](https://sixtynet.net/aff.php?aff=39) |
| LAX-Storage-500G | 4 / 4GB / 300GB + 200GB bonus, RAID 10 | 10TB | $400 (list $480) | [Order LAX-Storage-500G](https://sixtynet.net/aff.php?aff=39) |
| LAX-Storage-1TB | 8 / 8GB / 700GB + 300GB bonus, RAID 10 | 15TB | $700 (list $840) | [Order LAX-Storage-1TB](https://sixtynet.net/aff.php?aff=39) |
| Los Angeles China Unicom-Premium | AS9929, 100M base network, 3X burst | 95th percentile billing | $2,500 (list $3,000) | [Order China Unicom-Premium](https://sixtynet.net/aff.php?aff=39) |

Three things the table can't show. The residential plans carry a 13%–16% annual discount; LAX, Storage, IRVINE-PRO and China Unicom sit at a flat 17%. The Storage plans' second figure is free bonus capacity on the same RAID 10 array, not a separate disk. And IRVINE-PRO refunds land in your SixtyNet balance, not back on your card, which is a different policy from every other line.

Also worth flagging: LAX-LARGE is 8 cores with 16GB RAM, while Residential-LARGE is 16 cores with 16GB RAM. Same RAM, twice the cores, different product line, $60 difference per year. If you're comparing the two by spec sheet alone, that's the row people misread.

## Ports 80 and 443 are closed on all four residential plans

The official notice on each residential plan reads: "Due to IP risk control reasons, residential IP products do not open ports 80&443." In practice that means no public website, no standard HTTP or HTTPS service, and no Let's Encrypt HTTP challenge on those ports. Everything else runs normally. SSH, control panels on custom ports, API clients, automation scripts, social media management tools and crawlers don't need 80 or 443.

If a public site is part of your plan, buy LAX. It has no port restrictions and DDoS protection is already in the plan price, not an add-on.

IRVINE-PRO adds a second layer on top. SixtyNet describes it as rejecting all external probes and scans, with access restricted until you configure it. Only whitelisted IPs or port-forwarded devices get through. That's good for keeping the IP clean and bad if you expected to point a browser at it and see something.

Setup for either line follows the same two steps. Install or reinstall the OS in the client area at sixtynet.net/clientarea.php, then go to forward.sixtynet.net to configure ports and whitelist entries. SixtyNet keeps a knowledge base article on the residential security settings if you need the exact fields.

👉 [Compare the residential plans that fit an 80/443-free workload](https://sixtynet.net/aff.php?aff=39)

## The ISP behind the IP depends on the product line

SixtyNet's own plan page doesn't name an upstream ISP for any residential plan. Third-party writeups do, and they don't agree with each other: one describes the residential line as running on AT&T Mobility, another describes the Irvine residential security product as running on Cox Communications out of Rancho Santa Margarita in Orange County, and a third mentions Astound for a separate residential offering. All three can be true at once because they're different products.

That matters if you're buying for a specific platform's trust model. An AT&T Mobility mobile IP and a Cox home broadband IP behave differently against TikTok, ad platforms and banking fraud checks. Ask support which upstream sits behind the exact plan you're ordering before you pay for a year.

Other details from third-party testing, not from SixtyNet's page: the residential line tested without IPv6 support, with BBR enabled, and with disk I/O in the 168–188MB/s range on AMD EPYC hardware. Treat those as one tester's snapshot rather than a spec.

## Price check: where the $140/year numbers come from

Several 2026 reviews still list Residential-STARTER at $140/year, MICRO at $340, MEDIUM at $740 and LARGE at $1,540, along with a claimed 22% discount. SixtyNet's official page currently shows $260, $460, $860 and $1,660, with discounts between 13% and 16%.

The same reviews list LAX-STARTER at $200, LAX-MICRO at $400, LAX-MEDIUM at $800 and LAX-LARGE at $1,600, which match the official page exactly. A source that's right about four plans and wrong about four others usually isn't lying; it's stale. The residential section of those articles was written before a price change and never updated. Budget from the official figures and treat $140/year as a historical price.

Two policy details that affect what a year actually costs you. The refund window is **3 days**, not the 30 days most hosts advertise, so test the IP against your actual target platform in the first 72 hours. And if you buy IRVINE-PRO, the refund goes to your SixtyNet balance rather than your payment method.

👉 [See the verified annual prices on SixtyNet's plan page](https://sixtynet.net/aff.php?aff=39)

## Which plan fits which job

**Public website, WordPress, WooCommerce, a game server.** LAX, no question. LAX-STARTER at $200 handles a single small site with 5TB of traffic. Move to LAX-MICRO when you're running several sites or a database that needs more than 2GB of RAM. You don't need LAX-MEDIUM unless you're past 10TB of monthly traffic or genuinely short on cores.

**Social media management, SEO, scraping, affiliate tracking, anything that gets flagged for looking like a datacenter.** Residential. Residential-MICRO at $460 is the practical starting point if you're running automation software with a GUI or several browser profiles; Residential-STARTER's 2GB is tight for that. Residential-MEDIUM only makes sense once you're at 8 concurrent workloads. Most affiliate marketers never need Residential-LARGE's 16 cores.

**Chinese visitors plus a residential IP.** IRVINE-PRO is the only line that combines AS9929 China-optimized routing with a residential IP. IRVINE-PRO-STARTER at $350 covers a single-operator setup. Remember the whitelist requirement and the balance-only refund before you commit.

**Backups, media libraries, archives.** LAX-Storage-500G gives you 500GB usable on RAID 10 with 10TB of traffic for $400/year. If you need the space but not the CPU, this is cheaper than any compute plan with comparable storage. Skip it if you need fast database performance; RAID 10 on bulk storage isn't the same as a dedicated NVMe database volume.

**BGP peering, 95th percentile billing, China Unicom Premium transit.** The $2,500/year China Unicom-Premium plan is for network operators and businesses announcing their own IP space. It includes a free BGP session setup and limited BGP technical support, 100M base network with 3X burst, and 95th percentile billing. If you don't know what AS9929 or 95th percentile billing means, this plan isn't for you and nothing cheaper on the list is a substitute for it.

## FAQ

### How long is the refund window?

3 days from purchase. That's the whole window, and it's shorter than the 30 days most VPS hosts offer.

### Can I host a website on a residential plan?

Not on ports 80 or 443, which is what a normal browser expects. Use a LAX plan for anything public-facing.

### Does SixtyNet support IPv6?

Third-party testing of the residential line found no IPv6 support. SixtyNet's plan page doesn't advertise IPv6 on any line, so don't plan around it.

### Can I run Windows?

Windows is on the official OS list alongside CentOS, Debian, Ubuntu, Fedora, Arch Linux, openSUSE, AlmaLinux, FreeBSD, OpenBSD and CoreOS. Custom ISO uploads are supported, and there are one-click installers for cPanel, Plesk, CyberPanel, Webmin, Docker, WordPress and a few hundred others.

### Can I upgrade mid-term?

The VirtFusion control panel handles OS rebuilds, reboots, VNC console access and snapshots without a ticket. Third-party reviews describe moving between plans through the panel as straightforward; confirm the proration terms with support before you rely on it.

### Can I pay by credit card?

Reviews published in 2026 report that card payments were suspended for fraud-prevention reasons, with alternative methods available. SixtyNet's plan page doesn't state this, so check the checkout page before you plan around a specific card.

### Is the hardware actually current?

AMD EPYC processors, DDR4 3200MHz memory and NVMe storage across the range, KVM virtualization, in the Coresite LA2 facility in Los Angeles with Any2 peering. IOPS ratings run 12,500 on the smaller plans and 25,000 on the larger ones. Third-party reviews say the CPUs were recently upgraded to AMD 7K62.

## Before you order

Match the plan to the port requirement first, because it eliminates half the list immediately. If your workload needs a browser to reach it on 80 or 443, you're buying LAX. If it needs to look like a home connection to a platform, you're buying Residential or IRVINE-PRO, and you should confirm with support which upstream ISP sits behind that specific plan.

Second, put the 3-day refund window on your calendar. Install your actual software and test against your actual target platform on day one, not day three. And if IRVINE-PRO is on your shortlist, factor in that a refund returns to your SixtyNet balance rather than your card.

👉 [Start with the SixtyNet plan that matches your port requirements](https://sixtynet.net/aff.php?aff=39)
