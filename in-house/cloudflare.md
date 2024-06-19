---
description: Cloudflare Intelligence but via Discord
---

# Cloudflare

## intel

* Usage: `!intel`

Cloudforce One packages the vital aspects of modern threat intelligence and operations to make organizations smarter, more responsive, and more secure. Learn more at https://www.cloudflare.com/application-services/products/cloudforceone/

### intel domainhistory

* Usage: `!intel domainhistory <domain>`

Fetch and display category and domain history.

### intel ip

* Usage: `!intel ip <ip>`

Query intelligence on a public IP address.

### intel asn

* Usage: `!intel asn <asn>`

Fetch and display ASN intelligence from Cloudflare.

### intel domain

* Usage: `!intel domain <domain>`

Query Cloudflare API for domain intelligence.

### intel subnets

* Usage: `!intel subnets <asn>`

Fetch and display ASN subnets intelligence from Cloudflare.

### intel whois

* Usage: `!intel whois <domain>`

Query WHOIS information for a given domain.

## urlscanner

* Usage: `!urlscanner`

With Cloudflare’s URL Scanner, you have the ability to investigate the details of a domain, IP, URL, or ASN. Cloudflare’s URL Scanner is available in the Security Center of the Cloudflare dashboard, Cloudflare Radar and the Cloudflare API.\
\
Learn more at https://developers.cloudflare.com/radar/investigate/url-scanner/

### urlscanner scan

* Usage: `!urlscanner scan <url>`

Scan a URL using Cloudflare URL Scanner and return the verdict.

### urlscanner create

* Usage: `!urlscanner create <url>`

Start a new scan for the provided URL.

### urlscanner screenshot

* Usage: `!urlscanner screenshot <scan_id>`

Get the screenshot of a scan by its scan ID

### urlscanner search

* Usage: `!urlscanner search <query>`
* Restricted to: `ADMIN`

Search for URL scans by date and webpage requests.

### urlscanner har

* Usage: `!urlscanner har <scan_id>`

Fetch the HAR of a scan by the scan ID

### urlscanner results

* Usage: `!urlscanner results <scan_id>`

Get the result of a URL scan by its ID.
