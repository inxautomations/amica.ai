# Deployment & Availability

## Current Setup

Amica is currently hosted on a local machine (personal laptop) running:

* n8n (workflow automation server)
* Cloudflare Tunnel (to expose local server to the internet)

This setup allows external requests to reach the local n8n instance via a public URL.

## How It Works

1. n8n runs locally on the machine
2. Cloudflare Tunnel creates a secure public endpoint
3. Incoming requests are routed through the tunnel to the local server
4. Workflows process the request and return a response

## Availability Limitation

Since the system is hosted on a personal laptop, it is not always active.

* The service works **only when the local machine is running**
* Both **n8n and Cloudflare Tunnel must be active**
* If the system is offline, incoming requests will fail and throw an Error: Failed to fetch

## Current Status

* Development / Prototype environment
* Not deployed on a dedicated server or VPS
* Intended for testing and learning purposes

## Future Improvements

* Migrate to a VPS or cloud-based server for 24/7 uptime
* Improve reliability and availability
* Add monitoring and error handling
* Ensure stable public access without dependency on local machine

## Notes

This setup is intentional for early-stage development and experimentation, allowing rapid iteration without infrastructure cost.
