# AI Hardware Research & Performance Analysis Rules

## Project Scope
This project is dedicated to researching hardware for running Artificial Intelligence workloads (local LLM inference, fine-tuning, training, computer vision, and generative models) and analyzing hardware performance (memory bandwidth, VRAM capacity, compute throughput, power efficiency, and price-to-performance ratio).

---

## Mandatory Rules for Hardware Pricing & Verification

Whenever searching, fetching, quoting, or comparing hardware prices, the following rules **MUST** be strictly enforced:

### 1. Browser Environment & Session Isolation
- **Use This Computer's Browser**: Conduct all live price checking and page verification using this computer's browser tools (e.g., Playwright automation, headless Chromium/Firefox, or local browser sessions running on this machine).
- **Strictly Avoid Personal Profiles & Sessions**:
  - Never use, open, inspect, or attach to the user's personal browser profiles, cookies, login sessions, or saved credentials.
  - Always launch fresh, ephemeral, or isolated browser contexts (e.g., default Playwright isolated browser contexts, temporary user data directories, or incognito/private windows).

### 2. Stock Availability & Pricing Model Verification
- **Verified In-Stock Only**: Confirm that the hardware is genuinely available and in stock for purchase right now.
- **Exclude Ghost/Unavailable Inventory**: Do not list products that are out of stock, discontinued, or on indefinite backorder/pre-order without confirmed dispatch dates.
- **Strictly Exclude Bidding / Auction Listings**:
  - Never quote starting bids, active auction bids, or reserve prices (e.g., eBay auctions). Bidding prices do not reflect the actual final payable price.
  - Only quote fixed, immediate-purchase prices (e.g., eBay "Buy It Now" with `LH_BIN=1`, instant checkout, fixed-price retail, or confirmed Buy-It-Now second-hand listings) where the quoted price guarantees immediate purchase right now.
- Always report the merchant, purchase format (Buy It Now / Fixed Price), and current stock/availability status alongside the quote.

### 3. Shipping to Box Hill, Victoria, Australia
- **Destination**: Box Hill, Victoria, Australia (Postcode: **3128**).
- **Mandatory Shipping Inclusion**: All prices quoted must include or explicitly calculate the shipping and delivery fee to Box Hill, VIC 3128.
- **Total Landed Cost**: Clearly display:
  - Base item price (in AUD, specifying GST inclusion).
  - Shipping fee to Box Hill, VIC 3128 (or note if verified free delivery applies).
  - Final total landed cost in AUD.

### 4. Comparison Deliverable: Standalone HTML Report
- **Generate an HTML Report for Every Comparison**: For every hardware comparison or pricing analysis, generate a clean, self-contained, human-readable HTML file saved in the workspace (e.g., `index.html` or `<topic>_comparison.html`).
- **Mandatory HTML Report Sections**:
  - **Hardware & AI Performance Analysis**: Detailed comparison of AI capabilities (VRAM capacity, memory bandwidth, compute throughput, model support, and efficiency).
  - **Pricing & Landed Cost Breakdown**: Base price (AUD), shipping cost to Box Hill, VIC 3128, and total landed cost.
  - **Direct Purchase Links**: Clickable hyperlinks leading directly to the exact product/checkout pages where the hardware is currently available to purchase for the quoted price.
  - **Merchant & Stock Details**: Confirmed in-stock availability status and merchant name for each option.
- **Link in Conversation**: Always provide a direct clickable file URL (`file:///...`) to the generated HTML file in the chat response for quick opening in a browser.
