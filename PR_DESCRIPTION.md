# Implement List of Stores Feature - Backend API

Adds backend support for the "List of Stores" feature, allowing customers to view stores and sellers to manage their stores.

## Changes

- **Added Store Model** - One-to-one relationship with Customer
- **Created Store API** - Full CRUD operations (`/stores`)
- **Added Store Fixtures** - Sample data for testing
- **Fixed Product Bug** - Division by zero in `average_rating`

## API Endpoints

**GET /stores** - List all stores

```json
[
  {
    "id": 1,
    "name": "Steve's Electronics Store",
    "seller_name": "Steve Brownlee",
    "product_count": 59
  }
]
```

**POST /stores** - Create store (requires auth)

```json
{
  "name": "My Store",
  "description": "Store description"
}
```

## Testing

- [x] Run migrations and load fixtures
- [x] Test with: `curl http://localhost:8000/stores`
- [x] Verify authentication for POST/PUT
