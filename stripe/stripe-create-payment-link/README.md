# n8n Stripe Payment Link Workflow

## Overview
This n8n workflow automates the creation of a Stripe payment link. It starts with a Creation Form node, followed by a Config node to set up Stripe API credentials. The Create Stripe Product and Create Payment Link nodes generate the link, and the Respond to Webhook node handles responses.

## Setup
1. Add Your Credentials
2. Integrate your Stripe API credentials for secure communication.
3. Fill the Config Node
4. Configure the node with necessary parameters.

## Workflow Nodes
- Creation Form Node: Input details for the payment link.
- Config Node: Set up workflow configuration.
- Create Stripe Product Node: Generate a Stripe product.
- Create Payment Link Node: Create the payment link.
- Respond to Webhook Node: Handle Stripe webhook responses.
