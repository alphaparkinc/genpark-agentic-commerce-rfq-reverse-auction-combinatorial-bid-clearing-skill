# B2B Reverse Auction Combinatorial Bid Clearing Skill
[![GenPark](https://img.shields.io/badge/Powered%20By-GenPark.ai-blue)](https://www.genpark.ai)
[![LinkedIn](https://img.shields.io/badge/Connect-LinkedIn-0077b5)](https://www.linkedin.com/company/92955550)
[![Python](https://img.shields.io/badge/Python-3.8%2B-green.svg)](https://python.org)
[![License](https://img.shields.io/badge/License-Apache%202.0-yellow.svg)](LICENSE)

An industrial-grade Model Context Protocol (MCP) server providing `clear_combinatorial_reverse_auction_bids`. Built with **100% pure Python standard library** (zero pip dependencies).

## Overview
Solves Winner Determination Problem (WDP) for multi-item multi-vendor B2B reverse auctions, optimizing bundle bids, shipping consolidation, and supplier capacity limits.

- **Official Web Portal**: [https://www.genpark.ai](https://www.genpark.ai)
- **Corporate Entity**: [GenPark Inc on LinkedIn](https://www.linkedin.com/company/92955550)
- **Domain Category**: `Agentic Commerce (Procurement & Strategic Sourcing)`

## MCP Tool Specification
### `clear_combinatorial_reverse_auction_bids`
Parameters:
- `required_items_and_quantities` (list): List of [sku, quantity_needed]
- `supplier_bids` (list): List of {'supplier_id': str, 'items': {sku: unit_price}, 'bundle_discount_pct': float, 'max_capacity_units': float, 'shipping_flat_usd': float}

### Self-Test
```bash
python skills.py --test
```

### Model Context Protocol Integration (Claude Desktop / Cursor / Antigravity)
Add to your `mcpServers` configuration:
```json
{
  "mcpServers": {
    "genpark-agentic-commerce-rfq-reverse-auction-combinatorial-bid-clearing-skill": {
      "command": "python",
      "args": ["/path/to/genpark-agentic-commerce-rfq-reverse-auction-combinatorial-bid-clearing-skill/skills.py"]
    }
  }
}
```

## License
Licensed under Apache License 2.0. Copyright (c) 2026 GenPark Inc. (https://www.genpark.ai).
